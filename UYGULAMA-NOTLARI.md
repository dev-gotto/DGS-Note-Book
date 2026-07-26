# Uygulama Notları — v1.0.0 Yapısal Dönüşüm

Bu zip, repo ile birebir aynı dizin yapısındadır. İçindeki her şeyi aynı adlarla kopyalayıp üzerine yazabilirsin.

## Bu Zip'te Ne Var

- **434 yeni iskelet dosyası** — `docs/matematik/` altında 43 konu (M01'in 2 alt-konusu dahil 44 alt-konu klasörü), `docs/geometri/` altında 18 konu/alt-konu klasörü. Her alt-konu klasöründe 7 sayfa (`index.md`, `teorik.md`, `pratik.md`, `soru-bankasi.md`, `strateji.md`, `yaygin-hatalar.md`, `hizli-tekrar.md`), hepsi "İçerik yakında eklenecektir" notuyla.
- **`docs/hizli-tekrar.md`** — yeni üst düzey indeks sayfası.
- **`docs/index.md`** — yeni yapıya göre güncellendi.
- **`templates/konu/`** — yeni 7 dosyalık şablon klasörü.
- **`templates/metadata.yml`** — referans amaçlı güncellendi (artık ayrı dosya değil, front-matter alanlarının açıklaması).
- **`mkdocs.yml`** — `mkdocs-awesome-pages-plugin` ile güncellendi (61+ konuyu elle nav'a yazmak yerine otomatik).
- **`requirements.txt`** — plugin bağımlılığı eklendi.
- **`README.md`** — yeni yapı, 2 yeni kural (İskelet Kuralı, Konu Bölünme Kuralı) ve PD-008/009/010 eklendi.
- **`CHANGELOG.md`** — `v1.0.0` girişi eklendi.

## Elle Yapman Gereken İşlemler (silme)

Bu dosyalar yeni yapı tarafından **geçersiz kılındı**, ama zip içine "silinecek" bir dosya konulamadığı için elle silmen gerekiyor:

1. **`docs/matematik/M01-islem-yetenegi.md`** — eski tekil dosya (v1.1). Yerini `docs/matematik/M01-islem-yetenegi-ve-sayi-kumeleri/01-islem-yetenegi/` klasörü aldı.
2. **`templates/konu.md`** — eski tekil şablon. Yerini `templates/konu/` klasörü aldı.
3. (Önceki turdan hâlâ kalmışsa) **`commit-message.txt`** — kök dizindeki bu dosya `.github/commit-template.txt` ile çakışıyordu, önerimiz hâlâ geçerli.

## mkdocs.yml Hakkında Önemli Not

`mkdocs-awesome-pages-plugin` kurulu değilse (`pip install -r requirements.txt` çalıştırılmadan) site build **hata verir**. GitHub Actions workflow'u zaten `pip install -r requirements.txt` adımını içeriyor, bu yüzden Actions üzerinden deploy sorunsuz çalışmalı. Yalnızca yerelde `mkdocs serve` ile önizleme yapacaksan önce `pip install -r requirements.txt` çalıştırmayı unutma.

## Önerilen Commit Mesajı

```
docs: 61 konu için klasör bazlı 7-sayfa iskelet oluşturuldu

- M01, hocanın 2 videosuna göre 2 alt-konuya bölündü (islem-yetenegi, sayi-kumeleri)
- Diğer 60 konu, tek alt-konu varsayımıyla iskelet oluşturuldu (status: empty)
- docs/hizli-tekrar.md ana indeks eklendi
- templates/konu/ yeni 7 dosyalık şablon seti
- mkdocs.yml: awesome-pages-plugin eklendi (manuel nav yerine)
- README: İskelet Kuralı ve Konu Bölünme Kuralı eklendi (PD-008, PD-009, PD-010)
- Eski docs/matematik/M01-islem-yetenegi.md ve templates/konu.md kaldırıldı
```

## Sonraki Adım

Bu paket commit edildikten sonra sırada: `M01-islem-yetenegi-ve-sayi-kumeleri/01-islem-yetenegi/` ve `02-sayi-kumeleri/` alt-konularının **gerçek içeriğini**, elimizdeki `1__video.txt` ve `2__video.txt` transkriptlerinden, üzerinde anlaştığımız 5 katman + Soru Bankası + Hızlı Tekrar yapısına göre yazmak var.

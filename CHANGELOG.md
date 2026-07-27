# CHANGELOG

## v1.1.1 Navigasyon Düzeltmesi — matematik/ ve geometri/ 404 Sorunu

### Sorun
`mkdocs.yml`'deki `nav`, "Matematik" ve "Geometri" menü öğelerini
`matematik/` ve `geometri/` klasörlerine (dizin olarak) yönlendiriyor,
ancak bu klasörlerin kökünde bir `index.md` bulunmuyordu. Sonuç: GitHub
Pages üzerinde `/matematik/` ve `/geometri/` adresleri **404** dönüyordu.
Alt-konu sayfalarının (`M01.../01-islem-yetenegi/` vb.) doğrudan URL'leri
çalışıyordu, ama siteye üst menüden ("Matematik" linkine tıklayarak)
girildiğinde kullanıcı içeriğe ulaşamıyordu.

### Yapılanlar
- `docs/matematik/index.md` ve `docs/geometri/index.md` oluşturuldu:
  her iki dosya da kendi bölümündeki tüm konuları (43 Matematik,
  18 Geometri), durum simgeleriyle (`✅` tamamlandı, `🔎` gözden
  geçiriliyor, `✏️` taslak, `⏳` içerik bekleniyor) ve ilgili alt-konunun
  `index.md`'sine giden linklerle listeler.
- M01, tek satırlık bir konu yerine iki alt-konulu (İşlem Yeteneği,
  Sayı Kümeleri) nested bir liste olarak gösterilir, ikisi de `✅`.

### Bilinen, Henüz Çözülmemiş Konu
- `docs/matematik/M01-islem-yetenegi.md` — eski, tekil dosya (v1.1) hâlâ
  repoda duruyor; `v1.0.0` CHANGELOG girişinde elle silinmesi
  gerektiği belirtilmişti ama silinmemiş. Yeni yapıyla çakışmaz (farklı
  URL) ama siteye alakasız/eski bir sayfa olarak sızabilir; elle
  silinmesi önerilir.

## v1.1.0 M01 İçerik Tamamlandı

### Yapılanlar
- `M01-islem-yetenegi-ve-sayi-kumeleri/01-islem-yetenegi/` ve
  `02-sayi-kumeleri/` alt-konularının 7'şer sayfası (`index.md`,
  `teorik.md`, `pratik.md`, `soru-bankasi.md`, `strateji.md`,
  `yaygin-hatalar.md`, `hizli-tekrar.md`), `1__video.txt` ve
  `2__video.txt` transkriptlerinden gerçek içerikle dolduruldu.
- Her iki alt-konunun `index.md` front-matter'ı güncellendi:
  `status: complete`, `version: "1.0"`, `previous`/`next` linkleri
  alt-konular arasında (01 → 02) kuruldu, `references` alanına
  transkript dosya adları eklendi.
- `strateji.md` sayfalarına, `soru-bankasi.md`'den link verilen çözümlü
  örnekler için HTML anchor'lar (`ornek-1`..`ornek-4`) eklendi.
- Üst düzey `docs/hizli-tekrar.md` içindeki İşlem Yeteneği ve Sayı
  Kümeleri blokları "İçerik yakında eklenecektir" notundan çıkarılıp
  gerçek özetlerle güncellendi.

## v1.0.0 Yapısal Dönüşüm — Konu/Alt-Konu İskeleti

### Yapılanlar
- Ana referans listesindeki (`Dgs ders konuları.txt`) 61 konu, `M01–M43` (Matematik) ve `G01–G18` (Geometri) kodlarıyla eşlendi.
- Her konu için klasör bazlı bir yapı kuruldu: `docs/<matematik|geometri>/<KOD>-<slug>/<sıra-no>-<alt-konu-slug>/`.
- Her alt-konu klasöründe 7 sayfa iskeleti oluşturuldu: `index.md`, `teorik.md`, `pratik.md`, `soru-bankasi.md`, `strateji.md`, `yaygin-hatalar.md`, `hizli-tekrar.md`.
- M01 (İşlem Yeteneği ve Sayı Kümeleri), hocanın 2 ayrı videoda işlediği tespit edildiği için `01-islem-yetenegi` ve `02-sayi-kumeleri` olmak üzere 2 alt-konuya bölündü — bu, yeni "konu bölünme kuralı"nın ilk uygulanışı.
- Üst düzey `docs/hizli-tekrar.md` indeks sayfası eklendi: her konu için kısa kavram özeti + ilgili alt-konu hızlı-tekrar sayfasına link.
- `templates/konu/` yeni 7 dosyalık şablon seti ile güncellendi; eski `templates/konu.md` tekil şablonu artık kullanılmıyor.
- `mkdocs.yml`'e `mkdocs-awesome-pages-plugin` eklendi (61+ konuyu elle nav'a yazmanın sürdürülemez olması nedeniyle); `requirements.txt` güncellendi.
- `README.md`'ye iki yeni proje kuralı eklendi: (1) tüm konular için boş iskelet + "içerik yakında" bilgisi zorunluluğu, (2) içerik üretilirken bir konunun alt-konulara ayrıldığı fark edilirse yapının buna göre bölünmesi.

### Kaldırılanlar / Yerini Alanlar
- `docs/matematik/M01-islem-yetenegi.md` (tekil dosya, v1.1) — yeni klasör yapısındaki `M01-islem-yetenegi-ve-sayi-kumeleri/01-islem-yetenegi/` ile değiştirildi. Eski dosyanın elle silinmesi gerekiyor.
- `templates/konu.md`, `templates/metadata.yml` (eski tekil şablon) — `templates/konu/` klasörü ile değiştirildi; `metadata.yml` artık sadece referans amaçlı korunuyor (alanlar front-matter'a taşındı).

## v0.9.0 Content Structure Update

### Yapılanlar
- M01 İşlem Yeteneği dosyası şablonla (templates/konu.md) tam uyumlu hale getirildi: Pratik Bilgiler, Soru Çözüm Stratejileri, Yaygın Hatalar, Çözümlü Örnekler, Hızlı Tekrar, Kaynak ve Değişiklik Geçmişi bölümleri eklendi.
- M01 dosyasına metadata.yml şablonuna uygun front-matter eklendi (id, title, status, version, previous, next, references).
- docs/index.md genişletildi: proje amacı, konu durumu (Matematik/Geometri ilerleme listesi) ve kullanım rehberi eklendi.

## v0.8.1 Hotfix

### Yapılanlar
- GitHub Actions için contents: write izni eklendi.
- mkdocs.yml nav güncellendi.
- PRE_COMMIT_CHECKLIST eklendi.
- Teslim standardı AI_CONTEXT ve PROJECT_RULES dosyalarına eklendi.

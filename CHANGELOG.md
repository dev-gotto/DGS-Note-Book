# CHANGELOG

## v1.2.4 Transkript Teslim Yöntemi Netleştirildi — Sohbet Direktifi

### Yapılanlar
- "İçerik Doldurma Standardı" madde 1 güncellendi: transkript(ler)in
  repo içinde bir `uploads/` klasöründen değil, kullanıcı tarafından
  doğrudan sohbete dosya olarak yüklendiği netleştirildi; dosya adının
  `N__video.txt` formatında olması zorunluluğu kaldırıldı.
- "AI Asistanıyla Çalışma Kuralları" bölümüne **"Yeni Sohbet Direktifi
  (Örnek)"** alt bölümü eklendi: kullanıcının yeni bir sohbette içerik
  doldurma iş akışını başlatmak için yazması yeterli olan tek cümlelik
  örnek direktif belgelendi.

## v1.2.3 TOC Kaldırma Kararından Dönüldü — Türkçe Etiketleme

### Sorun / Karar Değişikliği
`v1.2.2`'de sağdaki "Table of contents" sidebar'ı tüm sayfalardan CSS ile
tamamen gizlenmişti. Kullanıcı geri bildirimiyle bunun aslında sayfa
içi başlıklara hızlı atlamayı sağlayan faydalı bir menü olduğu, sorunun
yalnızca **etiketin İngilizce olması** olduğu netleşti. Karar: menü
**kalacak**, yalnızca ismi Türkçeleştirilecek.

### Yapılanlar
- `mkdocs.yml` → `theme.language: tr` eklendi. Bu, mkdocs-material'ın
  yerleşik Türkçe çeviri paketini devreye sokar; "Table of contents"
  başlığı otomatik olarak **"İçindekiler"** olur (ayrıca arama,
  "sayfayı düzenle" gibi diğer arayüz metinleri de Türkçeleşir).
- `v1.2.2`'de eklenen `extra_css` girişi ve `docs/stylesheets/extra.css`
  dosyası **kaldırıldı** (artık kullanılmıyor).

### Elle Yapılması Gereken (önceki patch uygulandıysa)
`v1.2.2` patch'i daha önce uygulandıysa, `docs/stylesheets/extra.css`
dosyasının elle silinmesi gerekir (bu patch onu yeniden oluşturmaz,
yalnızca `mkdocs.yml`'i günceller).

## v1.2.2 Sağ "Table of Contents" Kaldırıldı

### Yapılanlar
- `docs/stylesheets/extra.css` eklendi: mkdocs-material'ın otomatik
  ürettiği sağ ikincil sidebar'ı (`.md-sidebar--secondary`, sayfa
  başlıklarından türeyen "Table of contents") global olarak gizler.
- `mkdocs.yml`'e `extra_css: [stylesheets/extra.css]` eklendi.
- Sayfalarımız kısa olduğu için bu menünün pratik faydası yoktu,
  yalnızca yatay alan kaplıyordu.

## v1.2.1 Sayfa Altı Navigasyon İyileştirmesi

### Sorun
Her sayfanın altındaki `[← Konu ana sayfasına dön](index.md)` linki
yalnızca geri dönüşü sağlıyordu; sıradaki sayfaya (ör. Teorik →
Pratik) geçmek için kullanıcı her seferinde konu ana sayfasına dönüp
oradan tekrar seçim yapmak zorundaydı.

### Yapılanlar
- `teorik.md`, `pratik.md`, `soru-bankasi.md`, `strateji.md` ve
  `yaygin-hatalar.md` dosyalarının alt navigasyonuna, `index.md`'deki
  "Sayfalar" sırasına (Teorik → Pratik → Soru Bankası → Strateji →
  Yaygın Hatalar → Hızlı Tekrar) uygun bir "sonraki sayfa" linki
  eklendi: `[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)`
  formatında. `hizli-tekrar.md` zincirin sonu olduğu için değişmedi.
- Bu değişiklik **305 dosyada** uygulandı: M01'in 2 tamamlanmış
  alt-konusundaki 10 dosya, geri kalan 60 boş iskelet konudaki 300
  dosya, ve `templates/konu/` şablonundaki 5 dosya (böylece bundan
  sonra oluşturulacak her yeni iskelet bu navigasyonu baştan içerir).
- README.md → "İçerik Doldurma Standardı" bölümüne bu kural
  ("Sayfa altı navigasyon") eklendi.

## v1.2.0 İçerik Doldurma Süreci Standartlaştırıldı

### Yapılanlar
- README.md'ye yeni bir **"İçerik Doldurma Standardı"** bölümü eklendi:
  bir konunun transkriptten 7 sayfaya nasıl dönüştürüleceğini (kaynak
  okuma → konu bölünme kontrolü → 7 sayfa → senkron dosyalar → patch →
  canlı doğrulama) adım adım tanımlar.
- `docs/matematik/index.md` ve `docs/geometri/index.md`, artık
  "Konu ve Alt-Konu Yapısı" bölümünde resmi olarak üçüncü indeks türü
  (bölüm indeksi) olarak tanımlandı.
- **PD-011 (Senkronizasyon Kuralı):** Bir alt-konu tamamlandığında üç
  dosyanın (alt-konu `index.md`, üst `hizli-tekrar.md`, bölüm `index.md`)
  aynı pakette güncellenmesi zorunlu hale getirildi.
- **PD-012:** `docs/matematik/index.md` / `docs/geometri/index.md`'nin
  `mkdocs.yml` nav'ı için zorunlu olduğu (yoksa 404) karar olarak
  belgelendi.
- Pre-Commit Checklist'e içerik-tamamlamaya özel 3 madde eklendi
  (front-matter, senkron dosyalar, anchor eşleşmesi).
- "AI Asistanıyla Çalışma Kuralları"na yeni madde eklendi: varsayılan
  odak artık açıkça roadmap sırasına göre içerik doldurma; ayrıca
  asistanın repoyu salt-okunur klonlayıp doğrudan doğrulama yapabileceği
  netleştirildi.
- Yol Haritası, M01'in tamamlandığını ve sıradaki hedefin
  `M02-tek-cift-sayilar-ve-isaret-incelemesi` olduğunu yansıtacak
  şekilde güncellendi.

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

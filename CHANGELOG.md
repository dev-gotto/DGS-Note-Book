# CHANGELOG

## v1.6.0 M05 İçerik Tamamlandı — Basamak Kavramı

### Yapılanlar
- `M05-basamak-kavrami/01-basamak-kavrami/` alt-konusunun 7 sayfası
  (`index.md`, `teorik.md`, `pratik.md`, `soru-bankasi.md`,
  `strateji.md`, `yaygin-hatalar.md`, `hizli-tekrar.md`),
  `8__video.txt` (Basamak Kavramı 1: çözümleme, benzetme, klasik
  kalıplar) ve `9__video.txt` (Basamak Kavramı 2: 4 işlem, sütun
  toplama/çıkarma bulmacaları, mantık soruları) transkriptlerinden
  gerçek içerikle dolduruldu. Konu Bölünme Kuralı kontrol edildi:
  `dgs ders konuları.txt`'de "basamak kavramı" tek bir referans madde
  olduğu ve her iki video da aynı konunun devamı olduğu için (M03/M04
  gibi) mevcut tek alt-konu klasörü (`01-...`) korundu, bölünme
  yapılmadı.
- Transkript uzunluğu (2 video, ~1800+ satır) nedeniyle PD-013 gereği
  iş iki adıma bölündü: önce `teorik.md` + `pratik.md`, ardından
  `strateji.md` + `yaygin-hatalar.md` + `soru-bankasi.md` +
  `hizli-tekrar.md` + senkron dosyalar.
- `index.md` front-matter'ı güncellendi: `status: complete`,
  `version: "1.0"`, `references` alanına `8__video.txt` ve
  `9__video.txt` eklendi (`previous`/`next` boş bırakıldı — tek
  alt-konulu bir konu olduğu için).
- `strateji.md` sayfasına, `soru-bankasi.md`'den link verilen 27
  çözümlü örnek için HTML anchor'lar (`ornek-1`..`ornek-27`) eklendi;
  örnekler çözümleme/benzetme (klasik kalıplar, katlı denklemler,
  boy-farkı problemi, basamak artış/azalışı, çarpımın basamak sayısı)
  ve 4 işlem (yanlış okunan rakamın etkisi, sütun toplama/çıkarma
  bulmacaları, rakam çiftleştirme, kibrit çöpü kısıtı, sayma temelli
  mantık soruları) konularını kapsıyor.
- `teorik.md`'ye basamak değeri/sayı değeri ayrımı, klasik çözümleme
  kalıpları tablosu (`AB+BA`, `AB-BA`, `ABC-CBA`, çevrimsel toplam),
  benzetme tanımı (baştan/sondan), çarpımın basamak sayısı kuralı ve
  standart kibrit çöpü (dijital gösterge) rakam-çöp sayısı tablosu
  eklendi.
- Üst düzey `docs/hizli-tekrar.md` içindeki basamak kavramı bloğu
  "İçerik yakında eklenecektir" notundan çıkarılıp gerçek özetle
  güncellendi (PD-011).
- `docs/matematik/index.md` içindeki ilgili satırın durum simgesi
  `⏳` → `✅` olarak güncellendi (PD-011, PD-012).
- `README.md`'deki "Yol Haritası" bölümünde M05 tamamlandı olarak
  işaretlendi, sıradaki hedef `M06-bolme-bolunebilme` olarak
  güncellendi.

## v1.5.1 Yazım Düzeltmesi — "faktörüyel" → "faktöriyel"

### Yapılanlar
- `dgs ders konuları.txt` kaynak listesindeki "faktörüyel" yazım hatası
  "faktöriyel" (doğru Türkçe yazım) olarak düzeltildi.
- Bu düzeltme, M04 konusuna ait tüm dosyalara (`README.md` hariç — orada
  yalnızca klasör yolu geçiyor) yayıldı: `index.md`, `teorik.md`,
  `pratik.md`, `strateji.md`, `yaygin-hatalar.md`, `soru-bankasi.md`,
  `hizli-tekrar.md` (M04 alt-konusu), üst düzey `docs/hizli-tekrar.md`
  ve `docs/matematik/index.md`.
- **Klasör adı (`M04-faktoruyel`) bilinçli olarak değiştirilmedi** —
  URL/link kırılmasını önlemek için; yalnızca görünen metinler
  (`title`, başlıklar, gövde metni) düzeltildi.

## v1.5.0 M04 İçerik Tamamlandı — Faktöriyel

### Yapılanlar
- `M04-faktoruyel/01-faktoruyel/` alt-konusunun 7 sayfası (`index.md`,
  `teorik.md`, `pratik.md`, `soru-bankasi.md`, `strateji.md`,
  `yaygin-hatalar.md`, `hizli-tekrar.md`), `6__video.txt` (Faktöriyel 1:
  kavram + sadeleştirme) ve `7__video.txt` (Faktöriyel 2: yorum
  soruları) transkriptlerinden gerçek içerikle dolduruldu. Konu Bölünme
  Kuralı kontrol edildi: `dgs ders konuları.txt`'de "faktöriyel" tek bir
  referans madde olduğu ve her iki video da aynı konunun devamı olduğu
  için (M03'teki gibi) mevcut tek alt-konu klasörü (`01-...`) korundu,
  bölünme yapılmadı.
- Transkript uzunluğu (2 video, ~1900+ satır) nedeniyle PD-013 gereği iş
  iki adıma bölündü: önce `teorik.md` + `pratik.md`, ardından
  `strateji.md` + `yaygin-hatalar.md` + `soru-bankasi.md` +
  `hizli-tekrar.md` + senkron dosyalar.
- `index.md` front-matter'ı güncellendi: `status: complete`,
  `version: "1.0"`, `references` alanına `6__video.txt` ve
  `7__video.txt` eklendi (`previous`/`next` boş bırakıldı — tek
  alt-konulu bir konu olduğu için).
- `strateji.md` sayfasına, `soru-bankasi.md`'den link verilen 26 çözümlü
  örnek için HTML anchor'lar (`ornek-1`..`ornek-26`) eklendi; örnekler
  sadeleştirme (bölme, toplama/çıkarmada parantez alma, pay/payda ayrı
  sadeleştirme, payda eşitleme), yorum (ardışık diziyi faktöriyele
  çevirme, `A!=k×B!` ve `P!/R!=5!` denklemleri, asal/asal olmayan
  tabanda üs bulma, sondan kaç basamağı `0`/`9`, negatif faktöriyel
  kısıtı) ve ÖSYM tarzı kombine sorular (demir blokları, dairelere
  rakam yazma, iki şart birden) konularını kapsıyor.
- `teorik.md`'ye ayrıca `0!=1` ispatı (kombinasyon formülüyle) ve
  Legendre mantığıyla asal çarpan sayısı bulma formülü eklendi.
- Üst düzey `docs/hizli-tekrar.md` içindeki faktöriyel bloğu "İçerik
  yakında eklenecektir" notundan çıkarılıp gerçek özetle güncellendi
  (PD-011).
- `docs/matematik/index.md` içindeki ilgili satırın durum simgesi
  `⏳` → `✅` olarak güncellendi (PD-011, PD-012).
- `README.md`'deki "Yol Haritası" bölümünde M04 tamamlandı olarak
  işaretlendi, sıradaki hedef `M05-basamak-kavrami` olarak güncellendi.

## v1.4.1 Limit Aşımını Önleme Kuralı Kalıcı Hale Getirildi (PD-013)

### Yapılanlar
- `README.md` → "Teslim Standardı" bölümüne **"Üretim ve Teslim Kuralları
  (Limit Aşımını Önleme)"** alt bölümü eklendi: transkriptin dosyadan
  okunması (chat'e yapıştırılmaması), üretilen içeriğin doğrudan repo
  dosyalarına yazılması (chat'e tam metin basılmaması), her dosyanın ayrı
  bir işlemle üretilmesi, teslimin yalnızca değişen dosyaların zip'i +
  kısa özet şeklinde yapılması ve olağan dışı uzun/çok parçalı
  transkriptlerde işin iki adıma bölünmesi kuralları kalıcı hâle
  getirildi. Bu kurallar, M03 içerik doldurma sohbetinde çıktı/mesaj
  limitinin aşılması sorunundan sonra eklendi.
- "Proje Kararları" tablosuna **PD-013** eklendi (yukarıdaki kuralın özeti).
- "AI Asistanıyla Çalışma Kuralları" madde 5'e PD-013'e çapraz referans
  eklendi.
- "Yeni Sohbet Direktifi (Örnek)" cümlesi **değiştirilmedi** — kurallar
  README'de kalıcı olduğu için kullanıcının her sohbette aynı kısa
  direktif cümlesini kullanması yeterlidir.

## v1.4.0 M03 İçerik Tamamlandı — Ardışık Sayılar

### Yapılanlar
- `M03-ardisik-sayilar/01-ardisik-sayilar/` alt-konusunun 7 sayfası
  (`index.md`, `teorik.md`, `pratik.md`, `soru-bankasi.md`, `strateji.md`,
  `yaygin-hatalar.md`, `hizli-tekrar.md`), `4__video.txt` ve
  `5__video.txt` transkriptlerinden gerçek içerikle dolduruldu. Konu
  Bölünme Kuralı kontrol edildi: hoca konuyu iki videoda tek bir bütün
  olarak (aynı konunun devamı) anlattığı için mevcut tek alt-konu
  klasörü (`01-...`) korundu, bölünme yapılmadı.
- `index.md` front-matter'ı güncellendi: `status: complete`,
  `version: "1.0"`, `references` alanına `4__video.txt` ve
  `5__video.txt` eklendi (`previous`/`next` boş bırakıldı — tek
  alt-konulu bir konu olduğu için).
- `strateji.md` sayfasına, `soru-bankasi.md`'den link verilen 14 çözümlü
  örnek için HTML anchor'lar (`ornek-1`..`ornek-14`) eklendi; örnekler
  farkların sabitliği (Argüman 1), toplam/ortadaki sayı (Argüman 2),
  terim bulma, hata düzeltme (artı yerine eksi), min-max aralık ve
  çarpımsal terimli seri kısayolu konularını kapsıyor.
- Üst düzey `docs/hizli-tekrar.md` içindeki ardışık sayılar bloğu
  "İçerik yakında eklenecektir" notundan çıkarılıp gerçek özetle
  güncellendi (PD-011).
- `docs/matematik/index.md` içindeki ilgili satırın durum simgesi
  `⏳` → `✅` olarak güncellendi (PD-011, PD-012).
- `README.md`'deki "Yol Haritası" bölümünde M03 tamamlandı olarak
  işaretlendi, sıradaki hedef `M04-faktoruyel` olarak güncellendi.

## v1.3.0 M02 İçerik Tamamlandı — Tek-Çift Sayılar ve İşaret İncelemesi

### Yapılanlar
- `M02-tek-cift-sayilar-ve-isaret-incelemesi/01-tek-cift-sayilar-ve-isaret-incelemesi/`
  alt-konusunun 7 sayfası (`index.md`, `teorik.md`, `pratik.md`,
  `soru-bankasi.md`, `strateji.md`, `yaygin-hatalar.md`, `hizli-tekrar.md`),
  `3__video.txt` transkriptinden gerçek içerikle dolduruldu. Konu Bölünme
  Kuralı kontrol edildi: hoca konuyu tek bir videoda anlattığı için mevcut
  tek alt-konu klasörü (`01-...`) korundu, bölünme yapılmadı.
- `index.md` front-matter'ı güncellendi: `status: complete`,
  `version: "1.0"`, `references` alanına `3__video.txt` eklendi
  (`previous`/`next` boş bırakıldı — M01'in son alt-konusunda olduğu gibi
  konular arası sıralama linklenmiyor, yalnızca aynı konunun alt-konuları
  arasında linkleniyor).
- `strateji.md` sayfasına, `soru-bankasi.md`'den link verilen 7 çözümlü
  örnek için HTML anchor'lar (`ornek-1`..`ornek-7`) eklendi; örnekler
  tek/çift yorum kısayolları (çift/tek katsayı, kuvvet silme, kesinlik
  yoksa değer verme, çok senaryolu dallanma) ve işaret incelemesi
  (kuvvet kısayoluyla işaret belirleme, çarpım/fark zinciri) konularını
  kapsıyor.
- Üst düzey `docs/hizli-tekrar.md` içindeki Tek-Çift Sayılar ve İşaret
  İncelemesi bloğu "İçerik yakında eklenecektir" notundan çıkarılıp
  gerçek özetle güncellendi (PD-011).
- `docs/matematik/index.md` içindeki ilgili satırın durum simgesi
  `⏳` → `✅` olarak güncellendi (PD-011, PD-012).
- `README.md`'deki "Yol Haritası" bölümünde M02 tamamlandı olarak
  işaretlendi, sıradaki hedef `M03-ardisik-sayilar` olarak güncellendi.

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

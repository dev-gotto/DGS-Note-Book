# DGS Note Book

> DGS Matematik ve Geometri için GitHub üzerinde geliştirilen, MkDocs Material ile yayınlanan, sürüm kontrollü bir dokümantasyon projesi.

---

# Proje Amacı

Bu proje, DGS Matematik ve Geometri konularını;

- düzenli,
- tekrar dostu,
- dokümantasyon kalitesinde,
- Git ile sürüm kontrollü

bir bilgi bankası haline getirmeyi amaçlar.

Video anlatımları ham kaynak olarak kullanılır. Nihai hedef, videolardan bağımsız olarak okunabilecek kaliteli bir referans oluşturmaktır.

---

# Teknolojiler

- Markdown
- MkDocs Material
- mkdocs-awesome-pages-plugin (61+ konuyu elle nav'a yazmamak için)
- GitHub Pages
- GitHub Actions

---

# Çalışma Akışı

```
Video → Transkript → Kullanıcı Notları → İçerik Analizi → Standart Dokümantasyon → Commit → GitHub Pages
```

---

# Konu İşleme Stratejisi

- Video sırası esas alınmaz; konu bütünlüğü esas alınır.
- Videolar yalnızca ham kaynaktır. Birden fazla video aynı konuya ait olabilir; bir video birden fazla konu içerebilir.
- Dokümantasyon, `Dgs ders konuları.txt` dosyasındaki 61 maddelik referans sıraya göre hazırlanır.

---

# Konu ve Alt-Konu Yapısı

Ana referans listesindeki her madde bir **konu** olur ve `M01`–`M43` (Matematik) veya `G01`–`G18` (Geometri) kodunu alır. Bir konu, hocanın videoda kendi ayırdığı şekilde bir veya daha fazla **alt-konuya** bölünebilir (bkz. "Konu Bölünme Kuralı" aşağıda).

```
docs/matematik/M01-islem-yetenegi-ve-sayi-kumeleri/
  01-islem-yetenegi/
    index.md            ← Amaç, sayfa linkleri, Kaynak, Değişiklik Geçmişi
    teorik.md            ← 📘 Teorik Bilgiler
    pratik.md             ← 💡 Pratik Bilgiler
    soru-bankasi.md      ← Geçmiş sınav soruları + ilgili çözüme link
    strateji.md          ← 🎯 Soru Çözüm Stratejileri
    yaygin-hatalar.md    ← ⚠️ Yaygın Hatalar
    hizli-tekrar.md      ← Alt-konuya özel hızlı tekrar
  02-sayi-kumeleri/
    (aynı 7 dosya)
```

Ayrıca üç adet **indeks sayfası** vardır, üçü de içerik büyüdükçe elle güncellenir:

- `docs/hizli-tekrar.md` — tüm konuların hızlı tekrar sayfalarına giden ve her biri için kısa bir kavram özeti içeren **ana indeks**.
- `docs/matematik/index.md` ve `docs/geometri/index.md` — kendi bölümündeki tüm konuları durum simgesiyle (✅/🔎/✏️/⏳) listeleyen **bölüm indeksleri**. Bunlar `mkdocs.yml`'deki `Matematik: matematik/` ve `Geometri: geometri/` nav girişlerinin çalışması için **zorunludur** — bu dosyalar olmadan `/matematik/` ve `/geometri/` adresleri 404 döner.

Bu üç dosya "Korunan Dosyalar" listesinde değildir ama şablon/iskelet dosyaları da değildir; içerik durumunu yansıtan **canlı indekslerdir** ve her konu tamamlandığında güncellenmesi gerekir (bkz. "İçerik Doldurma Standardı").

## Sayfa İçerikleri ve Kaynakları

| Sayfa | Kaynak | Amaç |
|---|---|---|
| 📘 Teorik Bilgiler | Matematiksel gerçekler | Değişmeyen tanım ve kurallar |
| 💡 Pratik Bilgiler | Hocanın anlatımı | Uygulama yöntemleri, kısayollar |
| Soru Bankası | Geçmiş gerçek DGS soruları | Biriktirilen soru havuzu, çözüme link |
| 🎯 Soru Çözüm Stratejileri | Hoca + genel best practice | Hocanın önerdiği + anlatmadığı iyi yöntemler |
| ⚠️ Yaygın Hatalar | Öğrenci hataları + ÖSYM'nin tuzakları | Hata örnekleri ve tuzağın derin kavrayışla çözümü |

Her alt-konunun `index.md` dosyasının başında front-matter bulunur (`id`, `title`, `status`, `version`, `previous`, `next`, `references` — alan referansı için bkz. `templates/metadata.yml`).

---

# Konu Kimlikleri

Matematik: `M01, M02, ..., M43`
Geometri: `G01, G02, ..., G18`

Kod, ana referans listesindeki sıraya birebir karşılık gelir (M=Matematik, G=Geometri). Bir konunun birden fazla alt-konuya bölünmesi kodu değiştirmez — bölünme yalnızca kod altındaki klasörde gerçekleşir (`01-...`, `02-...`).

---

# İçerik Doldurma Standardı

M01 ile birlikte kurulan ve artık standart kabul edilen iş akışı budur.
Yeni bir konunun içeriğini doldururken bu sıra izlenir:

1. **Kaynağı oku.** İlgili konunun transkript(ler)i kullanıcı tarafından
   sohbete doğrudan dosya olarak yüklenir (dosya adı serbesttir, ör.
   `3__video.txt`; repo içinde ayrı bir `uploads/` klasörü tutulmaz).
   Yüklenen transkript(ler) baştan sona okunur.
2. **Konu Bölünme Kuralı'nı kontrol et.** Transkript(ler) konunun
   hocanın videoda birden fazla alt-konuya ayrılıp ayrılmadığını
   gösteriyor mu? Gösteriyorsa iskelet önce buna göre bölünür (`01-...`,
   `02-...`), göstermiyorsa mevcut tek alt-konu klasörü kullanılır.
3. **7 sayfayı doldur** (her alt-konu için ayrı ayrı):
   - `teorik.md` — hoca anlatımından bağımsız, değişmeyen tanım/kural/formüller.
   - `pratik.md` — hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.
   - `strateji.md` — soru çözüm stratejileri + **çözümlü örnekler**. Her
     çözümlü örnek, başlığın hemen üstüne konan bir HTML anchor ile
     işaretlenir: `<a id="ornek-1"></a>` (ardından `## Örnek 1 — ...`).
     Bu anchor'lar `soru-bankasi.md`'den link almak içindir.
   - `yaygin-hatalar.md` — her madde "hata/tuzak örneği + derin kavrayışla
     çözüm" formatında yazılır.
   - `soru-bankasi.md` — tablo halinde, her satır `strateji.md#ornek-N`
     anchor'ına link verir.
   - `hizli-tekrar.md` — kısa madde madde özet.
   - `index.md` — Amaç metni yazılır; front-matter güncellenir
     (`status: complete`, `version: "1.0"`, `previous`/`next` komşu
     alt-konulara bağlanır, `references` alanına transkript dosya adı
     eklenir); Kaynak ve Değişiklik Geçmişi bölümleri doldurulur.

   **Sayfa altı navigasyon:** `teorik.md`, `pratik.md`, `soru-bankasi.md`,
   `strateji.md` ve `yaygin-hatalar.md` dosyalarının en altındaki
   `[← Konu ana sayfasına dön](index.md)` satırının sağına, sıradaki
   sayfaya giden bir link eklenir:
   `[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)`
   Sıra, `index.md`'deki "Sayfalar" listesiyle birebir aynıdır:
   Teorik → Pratik → Soru Bankası → Strateji → Yaygın Hatalar → Hızlı Tekrar.
   `hizli-tekrar.md` bu zincirin son halkasıdır, sonrasına link eklenmez.
   Bu kural, boş iskelet sayfalarında da (henüz içerik girilmeden)
   geçerlidir — `templates/konu/` şablonları bu linkleri zaten içerir.
4. **Senkron dosyaları güncelle (zorunlu, aynı pakette):**
   - `docs/hizli-tekrar.md` içindeki ilgili konunun bloğu
     ("İçerik yakında eklenecektir" yerine gerçek özet + link).
   - `docs/matematik/index.md` veya `docs/geometri/index.md` içindeki
     ilgili satırın durum simgesi (`⏳` → `✅`).
   - Bkz. PD-011 — bu üç dosyanın (alt-konu `index.md`, üst `hizli-tekrar.md`,
     bölüm `index.md`) senkron kalması zorunludur; biri güncellenip
     diğerleri unutulursa site tutarsız görünür.
5. **Patch'i hazırla ve teslim et** (bkz. "Teslim Standardı").
6. **Kullanıcı push ettikten sonra GitHub Pages'te doğrula:** hem
   derin link (`.../01-konu-adi/`) hem de üst menü üzerinden erişim
   (`Matematik` → bölüm indeksi → konu) test edilir. Bu adım özellikle
   yeni bir konu/alt-konu **ilk kez** tamamlandığında önemlidir (bkz.
   v1.1.1 navigasyon düzeltmesi, `CHANGELOG.md`).

---

# Çalışma Kuralları

- DGS konu sırasına uyulur; video sırası korunmaz.
- Konu bütünlüğü ve kullanıcının notları korunur.
- Eksik bilgiler yalnızca DGS kapsamı içerisinde tamamlanır.
- Kullanıcı istemedikçe proje mimarisi değiştirilmez.
- **İskelet Kuralı:** Tüm 61 konu için, içerik henüz üretilmemiş olsa bile, `templates/konu/` şablonuyla uyumlu boş bir iskelet (7 sayfa) baştan oluşturulur ve her sayfada içeriğin yakında ekleneceği açıkça belirtilir (`status: empty`). Bu, roadmap'in her zaman referans listesiyle birebir örtüşmesini sağlar.
- **Konu Bölünme Kuralı:** İçerik üretilirken, bir konunun hocanın anlatımında birden fazla alt-konuya (örn. birden fazla video) ayrıldığı fark edilirse, o konu iskeleti buna göre yeniden bölünür (`01-...`, `02-...` şeklinde yeni alt-konu klasörleri açılır). Bölünme, mevcut kod (M/G numarası) değişmeden, yalnızca klasör seviyesinde yapılır.
  - **Transkript Haritası Görünürlüğü:** Bölünme yapıldığı anda, hangi transkript dosyasının hangi alt-konuya ait olduğu iki yerde kalıcı olarak kaydedilir: (1) her alt-konunun `index.md` front-matter'ındaki `references:` alanında, ve (2) üst roadmap dosyasındaki (`docs/matematik/index.md` veya `docs/geometri/index.md`) ilgili satırda, alt-konu bağlantısının yanına parantez içinde kaynak video numarası eklenir (ör. `- ✏️ [bölme](.../01-bolme/index.md) — 10. video`). Amaç: bir konu birden fazla oturuma (sohbete) bölünerek işlenecekse, kullanıcının bir sonraki oturum için hangi transkripti yükleyeceğini roadmap dosyasına tekrar bakarak anlayabilmesi — bunun için yeni bir sohbet açıp Claude'a sorması ya da transkriptleri tekrar okutması gerekmez.

---

# AI Asistanıyla Çalışma Kuralları

Yeni bir sohbet başladığında:

1. README.md ve CHANGELOG.md okunur.
2. Son yapılan değişiklikler (roadmap, versiyon geçmişi) incelenir; `docs/matematik/index.md` ve `docs/geometri/index.md`'den hangi konuların `✅`, hangilerinin `⏳` olduğuna bakılır.
3. Mevcut mimari korunur; kullanıcı açıkça istemedikçe yeniden yapılandırma yapılmaz.
4. **Varsayılan odak artık içerik doldurmadır** ("İçerik Doldurma Standardı" bölümündeki 6 adım izlenir), roadmap sırasına göre bir sonraki `⏳` konu hedef alınır. Kullanıcı proje üzerine **analiz, gözlem veya öneri** isterse, bu doğrudan ve açıkça paylaşılır — sınırlı tutulmaz.
5. Teslimler `templates/` ve `docs/` dizin yapısına birebir uyan bir zip paketi olarak hazırlanır; asistanın repoya doğrudan yazma/commit erişimi yoktur, push işlemini kullanıcı yapar. Üretim sırasında sohbetin çıktı/mesaj limitini aşmamak için "Teslim Standardı" bölümündeki "Üretim ve Teslim Kuralları" (PD-013) uygulanır: içerik dosyalara yazılır, chat'e tam metin basılmaz.
6. Her teslime, hangi dosyanın üzerine yazılacağını ve elle yapılması gereken işlemleri (ör. dosya silme) açıklayan kısa bir not eşlik eder.
7. Repo'ya salt-okunur erişim (klonlama, doğrulama) serbesttir — README/CHANGELOG okumakla yetinilmez, gerektiğinde gerçek dosya/klasör yapısı ve GitHub Pages çıktısı doğrudan kontrol edilir.

## Yeni Sohbet Direktifi (Örnek)

İçerik doldurma işine yeni bir sohbette başlarken kullanıcının yazması
yeterli olan örnek direktif cümlesi:

> "DGS-Note-Book reposunu (https://github.com/dev-gotto/DGS-Note-Book/)
> klonla, README.md ve CHANGELOG.md'yi oku, roadmap'teki sıradaki `⏳`
> konuyu belirle. Transkript dosyasını yükleyeceğim, İçerik Doldurma
> Standardı'ndaki 6 adımı uygulayıp patch hazırla."

Bu cümle tek başına yeterlidir; asistan repoyu klonlar, roadmap'e göre
hedef konuyu kendisi tespit eder ve kullanıcının yükleyeceği transkripti
bekler.

---

# Teslim Standardı

Varsayılan teslim biçimi **Patch**'tir (ilgili dosyalar + değişiklik notu). Tam proje yalnızca ilk kurulumda veya kullanıcı açıkça istediğinde teslim edilir.

## Üretim ve Teslim Kuralları (Limit Aşımını Önleme)

İçerik doldurma gibi çok sayfalı işlerde sohbetin çıktı/mesaj limitinin
aşılmasını önlemek için aşağıdaki kurallar zorunludur (bkz. PD-013):

- Transkript(ler) her zaman **dosya olarak okunur**; ham metin chat
  mesajına yapıştırılmaz/kopyalanmaz.
- Üretilen 7 sayfanın (`teorik.md`, `pratik.md`, `strateji.md`,
  `yaygin-hatalar.md`, `soru-bankasi.md`, `hizli-tekrar.md`, `index.md`)
  ve senkron dosyaların içeriği **doğrudan klonlanan repo klasöründeki
  dosyalara** yazılır (dosya araçlarıyla); chat cevabına tam metin
  olarak basılmaz.
- Her dosya **ayrı bir işlemle** yazılır; tüm sayfalar tek seferde tek
  bir uzun mesajda üretilmeye çalışılmaz.
- Tüm adımlar bitince yalnızca **değişen/eklenen dosyalar** bir zip'e
  toplanır ve indirilebilir dosya olarak teslim edilir.
- Chat cevabında yalnızca **kısa bir özet** paylaşılır: hangi konu
  işlendi, hangi dosyalar değişti/eklendi, patch nasıl uygulanır, elle
  yapılması gereken bir şey var mı. Dosya içeriklerinin tamamı tekrar
  chat'e yazılmaz.
- Transkript alışılmadık derecede uzunsa veya konu birden fazla
  alt-konuya bölünüyorsa, iş tek seferde bitirilmeye çalışılmaz: önce
  iskelet + teorik + pratik, ardından strateji + yaygın hatalar + soru
  bankası + hızlı tekrar + senkron dosyalar şeklinde iki adıma bölünür.
- **Çok adımlı teslimde sekans kuralı:** İş iki veya daha fazla adıma
  bölündüğünde, her adımın çıktısı (o adıma ait dosyaların zip'i + kısa
  özet) kendi sırasında, ayrı bir teslim olarak verilir — sonraki adımın
  içeriği önceki adımla birleştirilip tek seferde sunulmaz. Bir sonraki
  adıma geçmeden önce kullanıcıdan açık onay istenir (ör. "1. adım
  [iskelet + teorik + pratik] teslim edildi, 2. adıma [strateji + yaygın
  hatalar + soru bankası + hızlı tekrar + senkron dosyalar] geçilsin
  mi?"); onay gelmeden bir sonraki adımın dosyaları üretilmez.

---

# Korunan Dosyalar

Aşağıdaki dosyalar yeniden oluşturulmaz, yalnızca güncellenir:

```
README.md
CHANGELOG.md
mkdocs.yml
```

---

# Pre-Commit Checklist

- Markdown dosyaları doğru klasörde mi?
- mkdocs.yml ve plugin listesi güncel mi?
- CHANGELOG güncellendi mi?
- Commit mesajı standarda uygun mu?
- GitHub Pages etkileniyor mu?
- Korunan dosyalar eziliyor mu?
- Yeni/bölünen konularda iskelet kuralına uyuldu mu?
- Paket Patch mi ve tek başına uygulanabilir mi?
- **[İçerik tamamlama'ya özel]** Alt-konu `index.md` front-matter'ı (`status`, `version`, `previous`/`next`, `references`) güncellendi mi?
- **[İçerik tamamlama'ya özel]** `docs/hizli-tekrar.md` ve ilgili bölüm indeksi (`docs/matematik/index.md` / `docs/geometri/index.md`) senkron mu (PD-011)?
- **[İçerik tamamlama'ya özel]** `strateji.md` örnek anchor'ları (`#ornek-N`) ile `soru-bankasi.md` linkleri eşleşiyor mu?
- **[İçerik tamamlama'ya özel]** Transkriptte çelişen/eksik/görsele dayanan bir kısım var mıydı; varsa PD-014'e göre mi ele alındı (ASR hatası → sürece uygun düzeltme; görsel-bağımlı belirsizlik → üretim durdurulup kullanıcıya video zaman aralığı bildirilerek soruldu mu)?

---

# Commit Mesaj Standardı

Referans şablon: `.github/commit-template.txt`

```
docs(M01): amaç ve teorik bilgiler eklendi
docs(M01): konu tamamlandı, şablon uyumu sağlandı
build(hotfix): fix GitHub Pages deploy
```

---

# Proje Kararları

| # | Karar |
|---|---|
| PD-001 | Video sırası yerine konu bütünlüğü esas alınır. |
| PD-002 | Bilgiler beş katmana ayrılır: Teori, Pratik, Soru Bankası, Strateji, Yaygın Hatalar. |
| PD-003 | Varsayılan teslim biçimi Patch'tir. |
| PD-004 | Korunan dosyalar yeniden oluşturulmaz. |
| PD-005 | Her teslim uygulanabilir bir değişiklik paketi olmalıdır. |
| PD-006 | Her iterasyon sonunda GitHub Pages üzerinden görünüm kontrol edilir. |
| PD-007 | AI asistanıyla çalışma kuralları, analiz/öneri taleplerini kısıtlamayacak; teslimler zip paketi + manuel commit olarak standartlaştırılmıştır. |
| PD-008 | Her konunun 5 bilgi katmanı (Teori, Pratik, Soru Bankası, Strateji, Yaygın Hatalar) ve Hızlı Tekrar, ayrı sayfalarda tutulur; konu bir klasörde toplanır. |
| PD-009 | Tüm 61 konu için, içerik üretilmeden önce boş iskelet (7 sayfa) oluşturulur ve "içerik yakında eklenecektir" notu paylaşılır. |
| PD-010 | İçerik üretimi sırasında bir konunun alt-konulara ayrıldığı fark edilirse, kod (M/G numarası) değişmeden klasör seviyesinde bölünme yapılır; hangi transkriptin hangi alt-konuya ait olduğu hem alt-konunun `index.md` front-matter'ındaki `references:` alanına hem de üst roadmap dosyasındaki ilgili satıra (parantez içinde video numarası olarak) yazılır (bkz. "Konu Bölünme Kuralı" → "Transkript Haritası Görünürlüğü"). |
| PD-011 | **Senkronizasyon Kuralı:** Bir alt-konu tamamlandığında (`status: complete`), aynı pakette üç yer birden güncellenir: alt-konunun kendi `index.md`'si, `docs/hizli-tekrar.md`'deki ilgili blok, ve `docs/matematik/index.md` / `docs/geometri/index.md`'deki durum simgesi. |
| PD-012 | `docs/matematik/index.md` ve `docs/geometri/index.md`, `mkdocs.yml` nav'ındaki `matematik/` ve `geometri/` dizin girişlerinin çalışması için zorunludur (yoksa GitHub Pages'te 404 oluşur); bu iki dosya da içerik ilerledikçe güncellenen canlı indekslerdir. |
| PD-013 | **Limit Aşımını Önleme Kuralı:** Transkript(ler) dosyadan okunur, chat'e yapıştırılmaz; üretilen sayfa/senkron dosyaların içeriği doğrudan repo klasörüne yazılır ve her dosya ayrı işlemle üretilir; teslim yalnızca değişen dosyaların zip'i + kısa özet şeklinde yapılır, dosya içerikleri chat'e tekrar basılmaz. İş birden fazla adıma bölündüğünde her adım kendi sırasında ayrı teslim edilir ve bir sonraki adıma geçmeden önce kullanıcıdan onay istenir (bkz. "Teslim Standardı"). |
| PD-014 | **Transkript Belirsizliği Protokolü:** İçerik üretimi sırasında transkriptte iki farklı türde güvenilmezlik ortaya çıkabilir; asistan bu ikisini ayırt etmek ve buna göre davranmak zorundadır: **(a) Basit ses-metin (ASR) hatası** — sayı/rakam gibi tek bir değerin yanlış tanınması (örn. aynı hesapta "357" ve "350" gibi çelişen iki değerin geçmesi). Bu durumda asistan, hocanın ulaştığı **nihai sonuçla ve anlattığı çözüm adımlarıyla hangi değer tutarlıysa onu doğru kabul eder**, düzeltir ve **kurguladığı içeriğin sürecin geri kalanıyla (verilen sayılar, ara adımlar, nihai cevap) birebir örtüştüğünden emin olur**; bunu sessizce yapar, sonuç teslim özetinde kısaca belirtilir. **(b) Ekran görseline/tabloya dayanan, sesten tam olarak yeniden kurulamayan içerik** — hocanın "şuraya bak, şu şurada" gibi işaret ifadeleriyle anlattığı, sayısal düzeni (hangi rakam hangi sütun/hücrede) transkriptten kesin olarak çıkarılamayan sorular (kibrit çöpü tabloları, sütun toplama/çıkarma bulmacaları, karşılaştırma görselleri vb.). Bu durumda asistan **tahmine dayalı bir soru metni uydurmaz**; üretimi o örnek için durdurur, kullanıcıya **hangi video ve hangi zaman aralığının (`mm:ss–mm:ss`) belirsiz olduğunu bildirir** ve kullanıcıdan ilgili kesiti izleyip doğru notu paylaşmasını ister. Kullanıcıdan onay/doğru içerik gelene kadar o örnek iskelet/taslak olarak işaretlenir, tamamlanmış muamelesi görmez. |


---

# Yol Haritası

## Altyapı
- [x] GitHub Repository
- [x] MkDocs Material + awesome-pages plugin
- [x] GitHub Pages
- [x] Konu/alt-konu klasör mimarisi (61 konu, 62 alt-konu iskeleti)
- [x] `docs/matematik/index.md` ve `docs/geometri/index.md` bölüm indeksleri (404 düzeltmesi, v1.1.1)

## İçerik
Durumu görmek için [docs/matematik/index.md](docs/matematik/index.md) ve
[docs/geometri/index.md](docs/geometri/index.md)'deki durum simgelerine
bakın (`✅` tamamlandı, `⏳` içerik bekleniyor).

- [x] `M01-islem-yetenegi-ve-sayi-kumeleri` — 2 alt-konu (İşlem Yeteneği, Sayı Kümeleri), `status: complete`
- [x] `M02-tek-cift-sayilar-ve-isaret-incelemesi` — 1 alt-konu, `3__video.txt` transkriptinden `status: complete`
- [x] `M03-ardisik-sayilar` — 1 alt-konu, `4__video.txt` ve `5__video.txt` transkriptlerinden `status: complete`
- [x] `M04-faktoruyel` — 1 alt-konu, `6__video.txt` ve `7__video.txt` transkriptlerinden `status: complete`
- [~] `M05-basamak-kavrami` — 1 alt-konu, `8__video.txt` ve `9__video.txt` transkriptlerinden `status: review` (23/27 örnek doğrulandı, 4 örnek PD-014b gereği kullanıcı video doğrulaması bekliyor — bkz. alt-konu `index.md`)
- [x] `M06-bolme-bolunebilme` — 2 alt-konu (bölme, bölünebilme kuralları), ikisi de `status: complete`; `01-bolme` `10__video.txt`'den, `02-bolunebilme-kurallari` `11__video.txt` ve `12__video.txt`'den
- [ ] `M07`–`M43`, `G01`–`G18` — iskelet hazır, içerik bekleniyor

Bundan sonraki her sohbette varsayılan iş: yukarıdaki listede sıradaki
`⏳` konunun transkriptini işleyip "İçerik Doldurma Standardı"ndaki
6 adımı uygulamak.

---

# Lisans

Kişisel eğitim amaçlı hazırlanmıştır.

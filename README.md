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

Ayrıca `docs/hizli-tekrar.md`, tüm konuların hızlı tekrar sayfalarına giden ve her biri için kısa bir kavram özeti içeren **ana indeks** sayfasıdır.

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

# Çalışma Kuralları

- DGS konu sırasına uyulur; video sırası korunmaz.
- Konu bütünlüğü ve kullanıcının notları korunur.
- Eksik bilgiler yalnızca DGS kapsamı içerisinde tamamlanır.
- Kullanıcı istemedikçe proje mimarisi değiştirilmez.
- **İskelet Kuralı:** Tüm 61 konu için, içerik henüz üretilmemiş olsa bile, `templates/konu/` şablonuyla uyumlu boş bir iskelet (7 sayfa) baştan oluşturulur ve her sayfada içeriğin yakında ekleneceği açıkça belirtilir (`status: empty`). Bu, roadmap'in her zaman referans listesiyle birebir örtüşmesini sağlar.
- **Konu Bölünme Kuralı:** İçerik üretilirken, bir konunun hocanın anlatımında birden fazla alt-konuya (örn. birden fazla video) ayrıldığı fark edilirse, o konu iskeleti buna göre yeniden bölünür (`01-...`, `02-...` şeklinde yeni alt-konu klasörleri açılır). Bölünme, mevcut kod (M/G numarası) değişmeden, yalnızca klasör seviyesinde yapılır.

---

# AI Asistanıyla Çalışma Kuralları

Yeni bir sohbet başladığında:

1. README.md ve CHANGELOG.md okunur.
2. Son yapılan değişiklikler (roadmap, versiyon geçmişi) incelenir.
3. Mevcut mimari korunur; kullanıcı açıkça istemedikçe yeniden yapılandırma yapılmaz.
4. Varsayılan odak içerik üretimi ve mevcut yapının geliştirilmesidir. Ancak kullanıcı proje üzerine **analiz, gözlem veya öneri** isterse, bu doğrudan ve açıkça paylaşılır — sınırlı tutulmaz.
5. Teslimler `templates/` ve `docs/` dizin yapısına birebir uyan bir zip paketi olarak hazırlanır; asistanın repoya doğrudan yazma/commit erişimi yoktur, push işlemini kullanıcı yapar.
6. Her teslime, hangi dosyanın üzerine yazılacağını ve elle yapılması gereken işlemleri (ör. dosya silme) açıklayan kısa bir not eşlik eder.

---

# Teslim Standardı

Varsayılan teslim biçimi **Patch**'tir (ilgili dosyalar + değişiklik notu). Tam proje yalnızca ilk kurulumda veya kullanıcı açıkça istediğinde teslim edilir.

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
| PD-010 | İçerik üretimi sırasında bir konunun alt-konulara ayrıldığı fark edilirse, kod (M/G numarası) değişmeden klasör seviyesinde bölünme yapılır. |

---

# Yol Haritası

## Altyapı
- [x] GitHub Repository
- [x] MkDocs Material + awesome-pages plugin
- [x] GitHub Pages
- [x] Konu/alt-konu klasör mimarisi (61 konu, 62 alt-konu iskeleti)

## İçerik
Tüm 61 konunun (43 Matematik + 18 Geometri) boş iskeleti oluşturuldu (`status: empty`). Hangi konunun içeriğinin tamamlandığını görmek için [docs/index.md](docs/index.md) → Durum bölümüne veya ilgili alt-konunun `index.md` front-matter'ındaki `status` alanına bakın.

İlk içerik hedefi: `M01-islem-yetenegi-ve-sayi-kumeleri` (2 alt-konu, kaynak transkriptler mevcut).

---

# Lisans

Kişisel eğitim amaçlı hazırlanmıştır.

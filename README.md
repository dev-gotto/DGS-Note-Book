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
- Dokümantasyon, DGS konu sırasına göre hazırlanır. Referans: `Dgs ders konuları.txt`

---

# İçerik Standardı

Her konu aynı yapıyı kullanır:

```
Konu → Amaç → 📘 Teorik Bilgiler → 💡 Pratik Bilgiler → 🎯 Soru Çözüm Stratejileri
→ ⚠️ Yaygın Hatalar → Çözümlü Örnekler → Hızlı Tekrar → Kaynaklar → Değişiklik Geçmişi
```

| Bölüm | İçerik |
|---|---|
| 📘 Teorik Bilgiler | Değişmeyen matematik kuralları: tanımlar, kurallar, formüller. |
| 💡 Pratik Bilgiler | Tecrübeye dayalı bilgiler: hız kazandıran yöntemler, kısayollar, eğitmen önerileri. |
| 🎯 Soru Çözüm Stratejileri | ÖSYM mantığı: şık kullanımı, eleme, tahmin, hızlı çözüm teknikleri. |
| ⚠️ Yaygın Hatalar | Öğrencilerin en sık yaptığı yanlışlar. |

Her konu dosyasının başında `templates/metadata.yml` ile uyumlu bir front-matter bulunur (`id`, `title`, `status`, `version`, `previous`, `next`, `references`).

---

# Konu Kimlikleri

Matematik: `M01, M02, M03, ...`
Geometri: `G01, G02, G03, ...`

---

# Çalışma Kuralları

- DGS konu sırasına uyulur; video sırası korunmaz.
- Konu bütünlüğü ve kullanıcının notları korunur.
- Eksik bilgiler yalnızca DGS kapsamı içerisinde tamamlanır.
- Kullanıcı istemedikçe proje mimarisi değiştirilmez.

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
- mkdocs.yml ve nav güncel mi?
- CHANGELOG güncellendi mi?
- Commit mesajı standarda uygun mu?
- GitHub Pages etkileniyor mu?
- Korunan dosyalar eziliyor mu?
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
| PD-002 | Bilgiler dört katmana ayrılır: Teori, Pratik, Strateji, Yaygın Hatalar. |
| PD-003 | Varsayılan teslim biçimi Patch'tir. |
| PD-004 | Korunan dosyalar yeniden oluşturulmaz. |
| PD-005 | Her teslim uygulanabilir bir değişiklik paketi olmalıdır. |
| PD-006 | Her iterasyon sonunda GitHub Pages üzerinden görünüm kontrol edilir. |
| PD-007 | AI asistanıyla çalışma kuralları, analiz/öneri taleplerini kısıtlamayacak; teslimler zip paketi + manuel commit olarak standartlaştırılmıştır. |

---

# Yol Haritası

## Altyapı
- [x] GitHub Repository
- [x] MkDocs Material
- [x] GitHub Pages
- [x] Dokümantasyon Mimarisi

## İçerik
- [x] M01 İşlem Yeteneği *(şablon tamamlandı — v1.1, içerik doğruluğu incelemesi bekleniyor)*
- [ ] M02 Sayı Kümeleri
- [ ] M03 ...
- [ ] G01 ...

---

# Lisans

Kişisel eğitim amaçlı hazırlanmıştır.

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

# Repository

https://github.com/dev-gotto/DGS-Note-Book

---

# Teknolojiler

- Markdown
- MkDocs Material
- GitHub Pages
- GitHub Actions

---

# Çalışma Akışı

```
Video

↓

Transkript

↓

Kullanıcı Notları

↓

İçerik Analizi

↓

Standart Dokümantasyon

↓

Commit

↓

GitHub Pages
```

---

# Konu İşleme Stratejisi

Video sırası esas alınmaz.

Konu bütünlüğü esas alınır.

Videolar yalnızca ham kaynaktır.

Birden fazla video aynı konuya ait olabilir.

Bir video birden fazla konu içerebilir.

Dokümantasyon DGS konu sırasına göre hazırlanır.

Referans:

```
Dgs ders konuları.txt
```

---

# İçerik Standardı

Her konu aynı yapıyı kullanır.

```
Konu

↓

Amaç

↓

📘 Teorik Bilgiler

↓

💡 Pratik Bilgiler

↓

🎯 Soru Çözüm Stratejileri

↓

⚠️ Yaygın Hatalar

↓

Çözümlü Örnekler

↓

Hızlı Tekrar

↓

Kaynaklar

↓

Değişiklik Geçmişi
```

---

## 📘 Teorik Bilgiler

Değişmeyen matematik kuralları.

Örnekler

- Tanımlar
- Kurallar
- Formüller
- Matematiksel açıklamalar

---

## 💡 Pratik Bilgiler

Tecrübeye dayalı bilgiler.

Örnekler

- Hız kazandıran yöntemler
- Kısa yollar
- Eğitmenin önerileri

---

## 🎯 Soru Çözüm Stratejileri

ÖSYM mantığı.

Örnekler

- Şık kullanımı
- Eleme
- Tahmin
- Hızlı çözüm teknikleri

---

## ⚠️ Yaygın Hatalar

Öğrencilerin en sık yaptığı yanlışlar.

---

# Konu Kimlikleri

Matematik

```
M01
M02
M03
...
```

Geometri

```
G01
G02
G03
...
```

---

# Çalışma Kuralları

- DGS konu sırasına uyulur.
- Video sırası korunmaz.
- Konu bütünlüğü korunur.
- Kullanıcının notları korunur.
- Eksik bilgiler yalnızca DGS kapsamı içerisinde tamamlanır.
- Kullanıcı istemedikçe proje mimarisi değiştirilmez.

---

# Assistant Startup Instructions

Yeni bir sohbet başladığında aşağıdaki adımlar izlenmelidir.

1. README.md dosyasını oku.
2. CHANGELOG.md dosyasını oku.
3. Son yapılan değişiklikleri incele.
4. Mevcut mimariyi koru.
5. Yeni öneriler sunma.
6. İçerik üretimine odaklan.

README.md bu proje için **Single Source of Truth** olarak kabul edilir.

---

# Teslim Standardı

Varsayılan teslim biçimi

```
Patch
```

Tam proje yalnızca

- ilk kurulumda
- kullanıcı açıkça istediğinde

teslim edilir.

---

# Korunan Dosyalar

Aşağıdaki dosyalar yeniden oluşturulmaz.

Yalnızca güncellenir.

```
README.md

CHANGELOG.md

mkdocs.yml
```

---

# Pre-Commit Checklist

Her teslimden önce aşağıdaki maddeler kontrol edilir.

- Markdown dosyaları doğru klasörde mi?
- mkdocs.yml güncel mi?
- nav güncel mi?
- CHANGELOG güncellendi mi?
- Commit mesajı hazır mı?
- GitHub Pages etkileniyor mu?
- Korunan dosyalar eziliyor mu?
- Paket Patch mi?
- Paket tek başına uygulanabilir mi?

---

# Commit Mesaj Standardı

```
docs(M01): amaç ve teorik bilgiler eklendi

docs(M01): pratik bilgiler eklendi

docs(M01): soru çözüm stratejileri eklendi

docs(M01): yaygın hatalar eklendi

docs(M01): konu tamamlandı

build(hotfix): fix GitHub Pages deploy
```

---

# Proje Kararları

PD-001

Video sırası yerine konu bütünlüğü esas alınır.

---

PD-002

Bilgiler dört katmana ayrılır.

- Teori
- Pratik
- Strateji
- Yaygın Hatalar

---

PD-003

Varsayılan teslim biçimi Patch'tir.

---

PD-004

Korunan dosyalar yeniden oluşturulmaz.

---

PD-005

Her teslim uygulanabilir bir değişiklik paketi olmalıdır.

---

PD-006

Her iterasyon sonunda GitHub Pages üzerinden görünüm kontrol edilir.

---

# Yol Haritası

## Altyapı

- [x] GitHub Repository
- [x] MkDocs Material
- [x] GitHub Pages
- [x] Dokümantasyon Mimarisi

## İçerik

- [ ] M01 İşlem Yeteneği
- [ ] M02 Sayı Kümeleri
- [ ] M03 ...

---

# Lisans

Kişisel eğitim amaçlı hazırlanmıştır.

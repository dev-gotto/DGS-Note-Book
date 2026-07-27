# 🎯 Soru Çözüm Stratejileri — İşlem Yeteneği

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Sahte Kural Tuzağı (ÖSYM Tarzı)

ÖSYM zaman zaman **yanlış bir işlem önceliği tanımlayan bir karakter**
üzerinden soru kurar (örn. "X öğrencisi işlem önceliğinin şöyle olduğunu
sanıyor: önce toplama, sonra çıkarma, sonra çarpma, sonra bölme").
Bu tip sorularda gerçek matematik kuralı değil, **soruda tanımlanan sahte
kural** uygulanmalıdır — soru metnini dikkatli okumak kritik önemdedir.

## Sembol/Şekil = 4 İşlem Sorularında Eleme Yöntemi

Daire, kare, beşgen gibi sembollerin toplama/çıkarma/çarpma/bölmeden
birini temsil ettiği sorularda:

1. Verilen sayısal eşitliklerden en "belirleyici" olanından başla
   (örn. küçük bir sayıyı büyük bir sonuca taşıyan eşitlik genelde
   çarpma ya da bölmeyi işaret eder).
2. Bir sembol için bir işlemi dene; sonuç tutmuyorsa o ihtimali ele.
3. Bir sembolün işlemini bulduğunda, diğer eşitliklerdeki yükü azaltmış
   olursun — kalan sembolleri aynı mantıkla çöz.

## "Seçilmeyen Sayı Hangisi Olamaz" Tipi Sorular

Bir grup sayıdan bazılarının seçilip bir eşitliği (`a/b = c - d` gibi)
sağladığı, geriye kalanın "seçilmeyen" olduğu sorularda:

1. En büyük sayıdan başlayarak, o sayı ile **tüm olası eşleşmeleri** tek
   tek dene (örn. önce 12 ile diğer tüm sayıları böl).
2. Bir sayı için tüm eşleşmeler denenip iş bittiğinde o sayıyı bir kenara
   bırak, bir sonraki büyük sayıyla devam et.
3. Her denemede "dışarıda kalan" sayıyı not et. Sorunun sorduğu
   ("hangisi kesinlikle **olamaz**") sayı, **hiçbir denemede dışarıda
   kalmayan** sayıdır.

Bu yöntem zaman alsa da tüm ihtimalleri sistematik şekilde tarar ve
yanlış cevap riskini sıfırlar.

---

<a id="ornek-1"></a>
## Örnek 1 — İşaret Kuralı ve Parantez İçi Öncelik

**Soru:** `(7 + 2) − 15` işleminin sonucu kaçtır?

**Çözüm:**
- Parantez içi önce hesaplanır: `7 + 2 = 9`
- Kalan ifade: `9 − 15` → farklı işaretli, büyükten küçük çıkarılır:
  `15 − 9 = 6`; büyüğün (15'in) işareti (−) sonuca yazılır.
- **Sonuç: −6**

<a id="ornek-2"></a>
## Örnek 2 — Parantez Dağıtma

**Soru:** `a − b + c − (a − b + c) + 2b` ifadesini sadeleştirin.

**Çözüm:**
- Parantez önündeki eksi dağıtılır: `a − b + c − a + b − c + 2b`
- `a` terimleri birbirini götürür, `c` terimleri birbirini götürür.
- Geriye `−b + b + 2b = 2b` kalır.
- **Sonuç: 2b**

<a id="ornek-3"></a>
## Örnek 3 — Çarpma/Bölme Sırası (Soldan Sağa)

**Soru:** `12 ÷ 4 × 3` işleminin sonucu kaçtır?

**Çözüm:**
- Çarpma ile bölme arasında öncelik yoktur; soldan sağa gidilir.
- Önce `12 ÷ 4 = 3`, sonra `3 × 3 = 9`.
- **Sonuç: 9** — Önce çarpmayı yapıp `12 ÷ (4×3) = 12 ÷ 12 = 1` demek
  **yaygın bir hatadır** (bkz. [⚠️ Yaygın Hatalar](yaygin-hatalar.md)).

<a id="ornek-4"></a>
## Örnek 4 — Üslü Sayılarda Parantezin Etkisi

**Soru:** `-2⁴` ile `(-2)⁴` ifadelerini karşılaştırın.

**Çözüm:**
- `-2⁴`: önce `2⁴ = 16` alınır, sonra baştaki eksi uygulanır → **−16**
- `(-2)⁴`: taban `-2`'dir, kuvvet çift ve parantez içindedir → **+16**

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

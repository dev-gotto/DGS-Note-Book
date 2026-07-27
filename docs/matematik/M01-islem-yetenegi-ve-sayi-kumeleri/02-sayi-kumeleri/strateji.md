# 🎯 Soru Çözüm Stratejileri — Sayı Kümeleri

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## "Hangisi Olamaz" Tipi Sıralama Soruları

Küçükten büyüğe bir sıralama verilip **"hangisi olamaz"** tipi soru
soruluyorsa, uç (en küçük/en büyük) değerlerden başlayarak sistematik
deneme yapılır; tüm ihtimaller tek tek tarandığında hiçbir yerde
çıkmayan değer cevaptır.

## Terazi/Sembol ile Verilen Sıralama Soruları

Verilen sıra bilgisine (`a < b < c` gibi) göre bir ortak katsayı (`k`)
atanarak en büyük/en küçük uç değerlerden (genelde `9` ya da `0`/`1`)
başlanır; sıradaki bir sonraki harfe geçmeden önce mevcut kısıtın
(örn. çarpımın belli bir sayıdan küçük olması) sağlanıp sağlanmadığı
kontrol edilir.

## Bölme İçeren Sorularda Sistematik Tarama

Paydası değişken olan ve bölme içeren sorularda önce ifade parçalanır
(tam kısım + kesirli kısım), sonra paydanın **bölen sayıları**
sistematik olarak (yarısına kadar) taranır — büyük sayılarda bu,
gereksiz denemeleri baştan eler.

## Toplam/Çarpım Sabit Sorularında Doğru Kuralı Seçme

Önce hangi büyüklüğün (toplam mı çarpım mı) **sorulduğu**, hangisinin
**sabit verildiği** ayırt edilir; "yakın seç / uzak seç" kararı buna göre
verilir (bkz. [💡 Pratik Bilgiler](pratik.md)).

---

<a id="ornek-1"></a>
## Örnek 1 — Rakamlarla En Küçük/En Büyük Değer

**Soru:** `a, b, c` birbirinden farklı rakamlar olmak üzere
`5a − 2b + 3c` ifadesinin en küçük değeri kaçtır?

**Çözüm:**
- En küçük değer için: çıkarılan terimin harfine (`b`) en büyük rakam
  (`9`), toplanan terimlerin harflerine (`a`, `c`) en küçük rakamlar
  (`0` ve `1`) verilir.
- `5(0) − 2(9) + 3(1) = 0 − 18 + 3 = −15`
- **Sonuç: −15**

<a id="ornek-2"></a>
## Örnek 2 — Çarpımı Sabit, Toplamı En Küçük

**Soru:** `x, y` doğal sayılar ve `x·y = 42` ise, `x + y` toplamının en
küçük değeri kaçtır?

**Çözüm:**
- 42'nin çarpan çiftleri: `(1,42), (2,21), (3,14), (6,7)`
- Çarpımı sabit sayılarda **birbirine en yakın** çift seçilirse toplam
  en küçük olur → `6` ve `7`
- `6 + 7 = 13` → **Sonuç: 13**

<a id="ornek-3"></a>
## Örnek 3 — Doğrusal Denklemde Tam Sayı Çözüm Sayısı

**Soru:** `x, y` doğal sayılar olmak üzere `3x + 5y = 60` eşitliğini
sağlayan kaç farklı `(x,y)` ikilisi vardır?

**Çözüm:**
- `y = 0` için `x = 20` (bir başlangıç çözümü)
- Sonraki çözümler: `x` **5'er 5'er azalırken**, `y` **3'er 3'er artar**
  (katsayılar ters yönde kaydırılır): `(20,0), (15,3), (10,6), (5,9), (0,12)`
- `x` doğal sayı olduğundan negatife inilemez, liste burada biter.
- **Sonuç: 5 farklı ikili**

<a id="ornek-4"></a>
## Örnek 4 — Parçalama ve Bölen Sayıları

**Soru:** `a, b` tam sayı olmak üzere `a = 2 + 10/b` ifadesine göre
`b`'nin alabileceği tam sayı değerleri nelerdir?

**Çözüm:**
- `b`, 10'un bölenidir: pozitif bölenler `1, 2, 5, 10`; tam sayı olduğu
  için negatif bölenler de eklenir: `-1, -2, -5, -10`
- **Toplam 8 farklı `b` değeri** vardır.
- `a`'nın alabileceği değerler toplamı kısa yoldan: sabit terim (`2`) ×
  bölen sayısı (`8`) = **16**

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

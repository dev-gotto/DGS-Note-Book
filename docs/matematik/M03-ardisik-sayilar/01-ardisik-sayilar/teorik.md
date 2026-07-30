# 📘 Teorik Bilgiler — ardışık sayılar

> Kaynak: Değişmeyen matematik kuralları (tanımlar, kurallar, formüller). Hoca anlatımından bağımsızdır.

## Ardışık Sayı Tanımı

**Ardışık sayı:** Artış miktarı sabit olan sayı dizileridir. Kilit nokta
"artış miktarının sabit olması"dır; ardışıklık yalnızca birer birer
artan sayılarla sınırlı değildir.

- **Ardışık tam sayılar:** artış miktarı `±1` (ör. `1, 2, 3, 4...`)
- **Ardışık tek sayılar:** artış miktarı `±2` (ör. `1, 3, 5, 7...`)
- **Ardışık çift sayılar:** artış miktarı `±2` (ör. `2, 4, 6, 8...`)
- **Genel ardışıklık:** Farkı sabit olan herhangi bir dizi de ardışıktır
  (ör. `2, 5, 8, 11...` artış miktarı `3` olan bir ardışık sayı dizisidir).

Artış yönü küçükten büyüğe de (`1, 2, 3`), büyükten küçüğe de (`4, 2, 1`
gibi negatif artışla) olabilir; önemli olan artışın **sabit** olmasıdır.

## Argüman 1 — Ardışık Sayıların Farkı Sabittir

`a, b, c` ardışık sayılarsa: `b - a = c - b` = sabit fark. Bu fark, dizinin
türüne göre değişir (tam sayıda `1`, tek/çift sayıda `2`, genel bir dizide
o dizinin artış miktarı).

## Terim Sayısı (Sayı Adedi) Formülü

```
Terim Sayısı = (Son Terim − İlk Terim) / Artış Miktarı + 1
```

Bu formül, ilk ve son terimler dahil olmak üzere aralıktaki toplam terim
sayısını verir. Artış miktarı `1` olduğunda (ardışık tam sayılar / birer
birer giden bir aralık) formül `Son − İlk + 1`'e indirgenir.

## Ortadaki Sayı

- **Terim sayısı tek** olduğunda, ortadaki sayı dizinin **gerçek bir
  üyesidir** (dizinin tam ortasındaki terim).
- **Terim sayısı çift** olduğunda, ortadaki sayı dizinin bir üyesi
  **değildir**; iki orta terimin aritmetik ortalamasıdır ("aradaki sayı").
- **Toplam biliniyorsa:** `Ortadaki Sayı = Toplam / Terim Sayısı`
- **Toplam bilinmiyorsa:** `Ortadaki Sayı = (İlk Terim + Son Terim) / 2`

## Argüman 2 — Ardışık Sayıların Toplamı

```
Toplam = Terim Sayısı × Ortadaki Sayı
```

Bilinen tüm toplam formülleri (`n(n+1)/2` dahil) temelde bu tek kurala
dayanır.

## Özel Toplam Formülleri

- **1'den n'e kadar ardışık doğal sayıların toplamı:**
  `n × (n + 1) / 2` (sondaki terim × bir fazlası, bölü 2)
- **1'den başlayan, n'e kadar giden ardışık tek sayıların toplamı**
  (n tek sayı olmalıdır): `((n + 1) / 2)²`
- **2'den başlayan, n'e kadar giden ardışık çift sayıların toplamı:**
  `(n / 2) × (n / 2 + 1)` (sondaki sayının yarısı × bir fazlası)

Bu üç formül de "terim sayısı × ortadaki sayı" temel kuralının özel
durumlarıdır; ezberlenmese de temel kuraldan türetilebilirler.

## İki Sabit Kural

1. **Ardışık İKİ sayının toplamı her zaman TEK sayıdır** — çünkü ardışık
   iki sayıdan biri mutlaka tek, diğeri mutlaka çifttir; tek + çift = tek.
2. **Terim sayısı TEK olan bir ardışık sayı grubunun toplamı, her zaman o
   terim sayısının katıdır.** Örneğin ardışık 3 sayının toplamı her zaman
   3'ün katıdır, ardışık 5 sayının toplamı her zaman 5'in katıdır. (Bu,
   "terim sayısı × ortadaki sayı" kuralının doğrudan bir sonucudur: terim
   sayısı tek olduğunda ortadaki sayı bir tam sayıdır ve toplam bu tam
   sayının terim-sayısı-katı olur.)

## 11 ile Çarpma Kısayolu (İki Basamaklı Sayılar İçin)

İki basamaklı bir sayı `11` ile çarpılırken, iki basamağın **arasına o
iki basamağın toplamı** yazılır:

- Toplam tek basamaklıysa (`0-9`) doğrudan araya yazılır.
- Toplam `10` veya üzerindeyse, birler basamağı araya yazılır ve elde
  kalan `1`, sol basamağa eklenir.

## 11'e Bölünebilme Kuralı (Üç Basamaklı Sayılar İçin)

Üç basamaklı bir sayının **ilk ve son basamağının toplamı, ortadaki
basamağa eşitse**, bu sayı `11`'e tam bölünür. Bölüm, sayının ilk ve son
basamaklarından oluşan iki basamaklı sayıdır (11 ile çarpma kısayolunun
tersidir).

[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)

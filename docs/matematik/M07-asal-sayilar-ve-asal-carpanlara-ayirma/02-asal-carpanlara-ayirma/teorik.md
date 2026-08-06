# 📘 Teorik Bilgiler — asal çarpanlara ayırma

> Değişmeyen matematik kuralları: tanımlar, kurallar, formüller.

## 1. Asal Çarpanlara Ayırma Tanımı (Aritmetiğin Temel Teoremi)

1'den büyük her doğal sayı, asal sayıların çarpımı biçiminde ve (çarpanların
sırası önemsenmezse) **tek bir şekilde** yazılabilir. Bu işleme **asal
çarpanlara ayırma** denir.

Genel gösterim:

$$N = a^{x} \cdot b^{y} \cdot c^{z} \cdots$$

Burada:

- $a, b, c, \dots$ birbirinden **farklı asal sayılardır**,
- $x, y, z, \dots$ bu asal sayıların $N$ içinde kaçar kez çarpan olarak
  bulunduğunu gösteren **pozitif tam sayı üslerdir**.

**Uygulama yöntemi:** Sayı, en küçük asal sayıdan başlanarak sırayla o
asal sayıya bölünür; bölüm artık bölünemez hale gelince bir sonraki asal
sayıya geçilir; bölüm 1 olana kadar devam edilir. Her asal sayıya kaç kez
bölündüyse, o asal sayının üssü o kadardır.

*Örnek:* $360 = 2^3 \cdot 3^2 \cdot 5^1$

## 2. Pozitif Bölen Sayısı Formülü

$N = a^{x} \cdot b^{y} \cdot c^{z}$ ise, $N$'nin **pozitif tam bölenlerinin
sayısı**:

$$d(N) = (x+1)(y+1)(z+1)$$

yani her üssün **birer fazlası alınıp çarpılır**.

## 3. Tam Sayı (Pozitif + Negatif) Bölen Sayısı

Bir sayının pozitif bölen sayısı kadar negatif böleni de vardır (her pozitif
bölenin karşılığı bir negatifi). Bu nedenle:

$$\text{tam sayı bölen sayısı} = 2 \cdot d(N)$$

## 4. Bölenler Toplamı Formülü

$N = a^{x} \cdot b^{y} \cdot c^{z}$ sayısının **pozitif bölenlerinin
toplamı**:

$$\sigma(N) = \left(\frac{a^{x+1}-1}{a-1}\right)\left(\frac{b^{y+1}-1}{b-1}\right)\left(\frac{c^{z+1}-1}{c-1}\right)$$

Küçük sayılarda pratikte bölenler tek tek yazılıp toplanabilir; büyük
sayılarda bu formül kullanılır.

## 5. Asal Bölenler ve Asal Bölenlerin Toplamı

$N = a^{x} \cdot b^{y} \cdot c^{z}$ sayısının **asal bölenleri**, üsler
dikkate alınmadan yalnızca **farklı** asal çarpanlardır: $a, b, c$.

- **Asal bölen sayısı** = farklı asal çarpan sayısı (üsler kaç olursa
  olsun her asal çarpan bir kez sayılır).
- **Asal bölenlerin toplamı** = $a + b + c$.

## 6. Özel Sayı Türleri (DGS'de Sık Geçen Tanımlar)

- **En büyük asal çarpanı $p$ olan sayı**, "**$p$'li sayı**" olarak
  adlandırılabilir (ör. $84 = 2^2 \cdot 3 \cdot 7$ sayısının en büyük
  asal çarpanı 7 olduğundan 84, 7'li bir sayıdır).
- Bir sayının **pozitif bölen sayısına tam bölünmesi** özel bir durumdur;
  böyle sayılar bazı kaynaklarda ayrı bir isimle anılabilir (ör. 12'nin
  6 pozitif böleni vardır ve 12, 6'ya tam bölünür).
- $N = a^{x} \cdot b^{y}$ biçimindeki bir sayının **tam kare** olabilmesi
  için gerek ve yeter koşul, tüm üslerin ($x, y, \dots$) **çift** sayı
  olmasıdır.

## 7. EBOB – EKOK ile İlişki

Asal çarpanlara ayırma, iki veya daha fazla sayının **EBOB**'unu (ortak
asal çarpanların **küçük** üsleriyle çarpımı) ve **EKOK**'unu (tüm asal
çarpanların **büyük** üsleriyle çarpımı) bulmanın temelini oluşturur.
Bu ilişkinin ayrıntılı işlenişi EBOB-EKOK konusundadır (bkz. M08).

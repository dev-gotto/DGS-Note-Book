# 📘 Teorik Bilgiler — faktöriyel

> Kaynak: Değişmeyen matematik kuralları (tanımlar, kurallar, formüller). Hoca anlatımından bağımsızdır.

## Faktöriyel Tanımı

**Faktöriyel** ("çarpansal"), `1`'den `n`'e kadar olan doğal sayıların
çarpımıdır ve `n!` şeklinde gösterilir:

```
n! = 1 × 2 × 3 × ... × n
```

Faktöriyel yalnızca **doğal sayılarda** tanımlı bir kavramdır; **negatif
sayılar için tanımlı değildir.**

## 0! = 1 (Özel Kabul)

Faktöriyel, doğal sayılarda `0`'dan başlar. `0!`, `1`'e eşit kabul
edilmiştir; bu, negatif sayılarda faktöriyel tanımlanamadığı için
matematikçilerin yaptığı özel bir kabuldür (ispatı için bkz. aşağıdaki
"0! = 1 İspatı").

## Temel Değerler

| n | n! |
|---|---|
| 0 | 1 |
| 1 | 1 |
| 2 | 2 |
| 3 | 6 |
| 4 | 24 |
| 5 | 120 |
| 6 | 720 |

## Ardışık Açılım Kuralı

Bir faktöriyel, kendisinden başlayarak birer birer azalan çarpanlara ve
sonunda durulan noktadaki faktöriyele ayrılarak açılabilir:

```
n! = n × (n-1)!
n! = n × (n-1) × (n-2)!
n! = n × (n-1) × (n-2) × ... × (k+1) × k!
```

Sayının kendisinden başlanır, birer birer azalınarak gidilir, durulan
yerde faktöriyel işareti konur. Bu açılım, iki faktöriyeli birbirine
benzetip **sadeleştirmenin** temelidir.

## İki Faktöriyelin Bölümü (Genel Formül)

`a > b` olmak üzere:

```
a! / b! = (b+1) × (b+2) × ... × a
```

Yani büyük faktöriyeli küçük faktöriyele bölmenin sonucu, küçük
faktöriyelden **sonraki** ardışık çarpanların çarpımıdır.

## Faktöriyel ve Kombinasyon İlişkisi

`n` elemandan `r` tanesini seçmenin (kombinasyon) formülü:

```
C(n, r) = n! / ((n - r)! × r!)
```

## 0! = 1 İspatı

`n`'in `n`'li kombinasyonu (`n` elemandan `n` tanesini seçmek), her
zaman `1`'dir (tek bir seçim şekli vardır — hepsini seçmek):

```
C(n, n) = n! / ((n - n)! × n!) = n! / (0! × n!) = 1
```

`n!` ifadeleri sadeleşince:

```
1 / 0! = 1
```

İçler dışlar çarpımı yapılırsa `0! × 1 = 1`, yani `0! = 1` bulunur.

## Faktöriyel İçindeki Asal Çarpan Sayısı (Legendre Mantığı)

`n!` içinde bir **asal sayı `p`'nin** kaç kez çarpan olarak geçtiğini
bulmak için, `n`, `p`'ye ardışık olarak bölünür ve bölüm sonuçları (kalan
değil) toplanır:

```
p'nin n! içindeki üssü = ⌊n/p⌋ + ⌊n/p²⌋ + ⌊n/p³⌋ + ...
```

(Bölme, bölünemeyecek noktaya kadar sürdürülür; her adımda yalnızca tam
bölüm alınır, kalan atılır.)

Taban **asal olmayan** bir sayıysa (ör. `6 = 2 × 3`), önce asal
çarpanlarına ayrılır; `n!` içindeki o bileşik sayının maksimum çarpan
adedi, asal çarpanlardan **sayıca daha az olanının** (büyük asal sayının)
üssüne eşittir — çünkü bir bileşik çarpan oluşturmak için her asal
çarpandan bir tane gerekir ve en az bulunan asal, oluşturulabilecek
bileşik çarpan sayısını sınırlar.

## Sondan Kaç Basamağının 0 Olduğu Kuralı

Bir sayının **sondan kaç basamağının `0` olduğu**, o sayının içinde kaç
tane `10 = 2 × 5` çarpanı olduğuna eşittir. `n!` içinde `2` çarpanı her
zaman `5` çarpanından fazla olduğundan, sondan kaç basamağının `0`
olduğu doğrudan **`n!` içindeki `5` çarpanı sayısına** eşittir (Legendre
formülüyle, `p = 5` alınarak bulunur).

## İşlem Sonucundaki Basamak Sayısı Kuralları

`n!` içeren toplama, çıkarma ve çarpma işlemlerinin sonucundaki sondan
`0` sayısı için:

- **Toplama:** İki (ardışık olmayan) faktöriyel toplanırken, sonucun
  sondan sıfır sayısı, **küçük olan faktöriyelin** sıfır sayısına eşittir.
- **Çarpma:** İki faktöriyel çarpılırken, sonucun sondan sıfır sayısı,
  ikisinin sıfır sayılarının **toplamına** eşittir.
- **Bölme:** İki faktöriyel bölünürken, sonucun sondan sıfır sayısı,
  ikisinin sıfır sayılarının **farkına** eşittir.
- **Ardışık faktöriyellerin toplamı/farkı** parantezine alınırken, açığa
  çıkan çarpanların içinde **yeni `5` çarpanları** oluşabilir; bu
  durumda küçüğü almak yeterli değildir, parantez içi ayrıca
  hesaplanmalıdır.

## Bir Sayıdan 1 Çıkarıldığında Basamakların 9 Olması

Sonu `k` tane `0` ile biten bir sayıdan `1` çıkarıldığında, sayının
sondan `k` basamağı `9` olur (ör. `1000 - 1 = 999`). Bu, `n!` sonu
`0`larla bitmesi gereken sorularda `n! - 1` gibi ifadelerin sondan kaç
basamağının `9` olduğunu sormak için kullanılır.

[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)

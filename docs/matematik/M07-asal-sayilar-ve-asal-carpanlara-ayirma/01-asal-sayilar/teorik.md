# 📘 Teorik Bilgiler — asal sayılar

> Değişmeyen matematik kuralları: tanımlar, kurallar, formüller.

## 1. Asal Sayı Tanımı

**Asal sayı**, 1'den ve kendisinden başka pozitif böleni olmayan, 1'den
büyük doğal sayıdır. Yani bir asal sayı yalnızca 1'e ve kendisine tam
bölünür.

- Asal sayılar **2'den başlar**: 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31,
  37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, ...
- **1 sayısı asal değildir.** Tanım gereği asal sayı 1'den büyük olmalıdır;
  1'in tek pozitif böleni kendisi olduğundan tanıma uymaz.
- 1'den büyük ve asal olmayan doğal sayılara **bileşik (asal olmayan) sayı**
  denir (4, 6, 8, 9, 10, 12, ...).
- Asal sayıların sayısı **sonsuzdur** (Öklid'in ispatı — DGS kapsamında
  ezber gerektirmez, bilgi amaçlıdır).

## 2. Asal Sayılarla İlgili 3 Temel Argüman

Sorularda tekrar tekrar kullanılan üç temel özellik:

1. **Bir asal sayının pozitif çarpanları yalnızca 1 ve kendisidir.**
   Bir çarpım asal bir sayıya eşitse, çarpanlardan biri kesinlikle 1,
   diğeri de o asal sayının kendisidir (negatif olmayan tam sayılar için).
2. **2'den başka çift asal sayı yoktur.** Her çift sayı 2'ye bölündüğü
   için, 2'nin dışındaki her çift sayının 1, kendisi ve 2 olmak üzere en
   az üç böleni vardır; dolayısıyla asal olamaz. Bu nedenle **2, tüm asal
   sayılar arasındaki tek çift sayıdır**; geri kalan bütün asal sayılar
   **tektir**.
3. **Farkı 1 olan (ardışık) asal sayı çifti yalnızca 2 ve 3'tür.** 2'den
   sonra gelen tüm asal sayılar tek olduğundan, iki ardışık doğal sayının
   asal olabilmesi için biri çift biri tek olmalıdır; bu da yalnızca
   2 ile 3 için mümkündür.

## 3. Bir Sayının Asal Olup Olmadığını Test Etme Yöntemi

Bir $n$ doğal sayısının asal olup olmadığını anlamak için:

1. Asal sayıları küçükten büyüğe sıralayıp karelerini yazın: $2^2=4,\ 3^2=9,\ 5^2=25,\ 7^2=49,\ 11^2=121,\ 13^2=169,\ 17^2=289, \dots$
2. $n$ sayısının hangi iki ardışık asal sayı karesi arasında kaldığını
   bulun (yani $p_k^2 < n < p_{k+1}^2$ olacak şekilde $p_k$'yı belirleyin).
3. $n$, bu noktaya kadar sıralanan asal sayıların **hiçbirine** tam
   bölünmüyorsa **asaldır**; en az birine bölünüyorsa **asal değildir**.

Bu yöntem, $\sqrt{n}$'den küçük veya ona eşit asal sayılara bölünüp
bölünmediğine bakmanın pratik bir uygulamasıdır: eğer $n$'nin
$\sqrt{n}$'den büyük bir asal çarpanı olsaydı, eşleniği olan diğer çarpanı
$\sqrt{n}$'den küçük olmak zorunda kalırdı — dolayısıyla $\sqrt{n}$'ye
kadar olan asal sayıları kontrol etmek yeterlidir.

## 4. Aralarında Asal (Kendi Aralarında Asal) Sayılar

İki pozitif tam sayının **1'den başka ortak (pozitif) böleni yoksa**, bu
iki sayıya **aralarında asal** (kendi aralarında asal) denir. Matematiksel
olarak, $a$ ve $b$ aralarında asaldır ⇔ $\text{EBOB}(a,b) = 1$.

- Aralarında asallık, sayıların kendisinin asal olup olmamasından
  **bağımsızdır**: iki sayı da asal olabilir (7 ve 12'deki gibi asal
  olmayanlarla da), biri asal biri asal olmayan olabilir (7 ile 12), ya
  da ikisi de asal olabilir (13 ile 17). Belirleyici olan **ortak asal
  çarpan bulunmamasıdır**, sayıların kendi asallığı değil.
- **Ardışık iki doğal sayı her zaman aralarında asaldır** (aralarındaki
  fark 1 olduğundan, ortak bir böleni olsaydı bu bölen 1'i de bölmek
  zorunda kalırdı).

### Oran Eşitliklerinde Kullanımı

$a, b$ pozitif tam sayılar ve $x, y$ aralarında asal (yani sadeleşmeyen,
en sade haldeki) pozitif tam sayılar olmak üzere,

$$\frac{a}{b} = \frac{x}{y}$$

eşitliği varsa, bu oranı sağlayan sonsuz sayıda $(a,b)$ çifti vardır; genel
çözüm bir $k$ pozitif tam sayısı için $a = k\cdot x,\ b = k\cdot y$
biçimindedir. Sorularda $a$ ve $b$'nin **kendisinin de aralarında asal
olduğu** ayrıca belirtilmişse, bu durumda sadeleşme kalmadığından
$k = 1$ olmak zorundadır ve doğrudan $a = x,\ b = y$ yazılabilir.

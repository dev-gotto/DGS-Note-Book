# 💡 Pratik Bilgiler — asal sayılar

> Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## 1. "Çarpım Asalsa" Kısayolu

Bir soruda iki ifadenin çarpımı (veya toplam/farkın parçalara ayrılmış
hali) bir asal sayıya eşitleniyorsa, direkt olarak:

- **Çarpanlardan biri 1, diğeri o asal sayının kendisidir.**
- Negatif olasılıkları elemek için genelde "pozitif tam sayı" şartı
  verilir; bu şart varsa, çarpanı 1 yapan tarafı (küçük olan) seçin,
  diğer tarafı asal sayının kendisine eşitleyin.

Örnek kalıp: $a - 2$ ve $b + 5$ ifadelerinin çarpımı 13 (asal) ise,
$a - 2 = 1$ ve $b + 5 = 13$ alınır (tam tersi, negatif bir değer
doğuracağından elenir).

## 2. "Asal Sayıların Toplamı" Kısayolu

Üç veya daha fazla asal sayının toplamının **çift** çıktığı sorularda:

1. Hepsinin tek olduğunu varsayarsanız toplam **tek** çıkar — bu, çift
   sonuçla çelişir.
2. Demek ki sayılardan **tam olarak biri çift** olmalıdır.
3. Asal sayılar içinde çift olan **tek sayı 2'dir** → o sayı 2'dir.
4. Sayılar küçükten büyüğe sıralıysa (ör. $a < b < c$), en küçük olan
   zaten 2'den küçük olamayacağı için **en küçük harf otomatik olarak
   2'dir**.

Bu kısayol, hem "toplamları verilmiş, iki tanesinin toplamını bul" hem de
doğrudan üç değişkenin toplamını isteyen sorularda kullanılır.

## 3. "Farkları 1" Kısayolu

Bir soruda iki asal sayının **farkının 1** olduğu (ya da $a - b$ gibi bir
ifadenin 1'e eşitlendiği) görülürse, aralarındaki tek olasılık **2 ve 3**'tür
(küçük olan 2, büyük olan 3). Bu genellikle çarpanlarına ayrılmış ifadelerde
(örn. iki kare farkı $a^2-b^2=(a-b)(a+b)$) asal sayıya eşitleme
sorularıyla birlikte çıkar: çarpanlardan biri 1 (küçük fark), diğeri asal
sayının kendisi olduğunda, aynı zamanda 1 farkı bulunan iki asal sayı
gerekiyorsa doğrudan 2 ve 3 yazılır.

## 4. Asal Sayı Testi — Hızlı Uygulama

"241 sayısı asal mıdır?" tarzı bir soruda uzun uzun tüm asal sayılara
bölmek yerine:

1. Asal sayı karelerini yazın: $4, 9, 25, 49, 121, 169, 289, \dots$
2. Sorulan sayının hangi iki kare arasında kaldığını bulun (241 için
   $169 < 241 < 289$, yani sınır 17'dir).
3. O sınıra kadar olan asal sayılara (2, 3, 5, 7, 11, 13, 17 → 241 için
   sınır 17 olduğundan 17 dahil, karesi sayıyı geçen ilk asal hariç)
   tek tek bölünüp bölünmediğine bakın; bölünebilirlik kurallarını
   (2, 3, 5, 11 için hazır kurallar) kullanarak hızlı eleyin.
4. Hiçbirine bölünmüyorsa sayı **asaldır**.

Soru doğrudan "asal mıdır?" değil de "**kaç tane** asal sayıya bölünüp
bölünmediği kontrol edilmelidir?" şeklinde soruluyorsa, cevap doğrudan bu
listedeki asal sayı **sayısıdır** — sayının kendisinin asal olup olmadığını
bulmaya gerek kalmadan sayılabilir.

## 5. Aralarında Asal Oranlarda Doğrudan Eşleme

$a/b = x/y$ biçiminde bir eşitlik verilip $x$ ile $y$'nin aralarında asal
(sadeleşmeyen) olduğu belirtilmişse:

- $a$ ve $b$'nin **kendisinin de** aralarında asal olduğu ayrıca
  söyleniyorsa → doğrudan $a = x$, $b = y$ yazılır.
- $x/y$ sadeleşiyorsa (aralarında asal değilse), önce sadeleştirip sonra
  eşleme yapılır.
- $7a = 4b$ gibi "içler dışlar" formunda verilmiş bir eşitlik görülürse,
  bunu orana çevirin ($a/b = 4/7$) ve aynı kısayolu uygulayın: payda
  değişkenine payın sayısal değeri, paya da paydanın sayısal değeri
  verilir (değiş-tokuş mantığı).

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

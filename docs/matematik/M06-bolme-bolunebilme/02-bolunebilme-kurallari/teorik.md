# 📘 Teorik Bilgiler — bölünebilme kuralları

DGS müfredatında **kendine ait, doğrudan bölünebilme kuralı olan** sayılar şunlardır: **2, 3, 4, 5, 8, 9, 10 ve 11**. Bunların dışında (6, 7, 12, 13, ... gibi) hiçbir sayının kendine özgü bir bölünebilme kuralı yoktur — bu sayılarla ilgili sorular "Kuralı Olmayan Sayılar" bölümündeki çarpanlara ayırma yöntemiyle çözülür.

## 2 ile Bölünebilme

Bir sayının **birler basamağı** çift (0, 2, 4, 6, 8) ise sayı 2'ye tam bölünür.
Birler basamağı tek ise, sayının 2'ye bölümünden kalan **1**'dir.

## 3 ile Bölünebilme

Bir sayının **rakamlarının toplamı** 3'ün katı ise, sayı 3'e tam bölünür.
Değilse, sayının 3'e bölümünden kalanı bulmak için sayının kendisi değil, **rakamları toplamı** 3'e bölünür; çıkan kalan sayının kalanına eşittir.

## 4 ile Bölünebilme

Bir sayının **son iki basamağı** (son iki basamağın oluşturduğu iki basamaklı sayı) 4'ün katı ise, sayı 4'e tam bölünür.
Değilse, sayının 4'e bölümünden kalanını bulmak için sayının tamamı değil, yalnızca **son iki basamağı** 4'e bölünür.

## 5 ile Bölünebilme

Bir sayının **birler basamağı** 0 ya da 5 ise, sayı 5'e tam bölünür.
Değilse, sayının 5'e bölümünden kalanını bulmak için yalnızca **birler basamağı** 5'e bölünür (kalan 1, 2, 3 veya 4 olabilir).
Pratik sonuç: bir sayının 5'e bölümünden kalanı 2 ise, sayının son rakamı ya **2** ya da **7**'dir (kalanı $k$ olan sayının son rakamı $k$ ya da $k+5$'tir).

## 8 ile Bölünebilme

Bir sayının **son üç basamağı** 8'in katı ise, sayı 8'e tam bölünür.
Değilse, sayının 8'e bölümünden kalanını bulmak için yalnızca **son üç basamağı** 8'e bölünür.

## 9 ile Bölünebilme

Bir sayının **rakamlarının toplamı** 9'un katı ise, sayı 9'a tam bölünür (yöntem 3 ile aynıdır).
Değilse, sayının 9'a bölümünden kalanını bulmak için **rakamları toplamı** 9'a bölünür.

## 10 ile Bölünebilme

Bir sayının **birler basamağı** 0 ise, sayı 10'a tam bölünür.
Değilse, sayının 10'a bölümünden kalanı doğrudan sayının **birler basamağıdır** (5 kuralından farklı olarak burada tek bir ihtimal vardır, çünkü her rakam 10'a bölündüğünde kendi değerini kalan olarak verir).

## 11 ile Bölünebilme

Bir sayının rakamları **sağdan sola doğru** sırayla artı-eksi-artı-eksi... işaretiyle işaretlenip toplanır (ilk işaret, en sağdaki rakamda, her zaman **artı**dır). Çıkan sonuç:

- **0** ise, sayı 11'e tam bölünür.
- **0 ile 11 arasında pozitif bir değer** ise, bu değer doğrudan 11'e bölümünden kalandır.
- **11 veya daha büyük** çıkarsa, sonuçtan 11 çıkarılarak (gerekirse tekrar tekrar) 0–11 aralığına indirilir.
- **Negatif** çıkarsa, sonuca 11 eklenerek (gerekirse tekrar tekrar) 0–11 aralığına indirilir.

**3 basamaklı sayılar için kısayol:** $\overline{abc}$ sayısında, baştaki ile sondaki rakamın toplamı ($a+c$) ortadaki rakamı ($b$) veriyorsa, sayı 11'e tam bölünür. Vermiyorsa, $a+c-b$ hesabının sonucu (0 ya da 11 ise tam bölünür, değilse) doğrudan kalanı verir.

## Kuralların Neden Böyle Olduğu (Kanıt Mantığı)

**2, 4, 8 için:** Bu sayılar sırasıyla $2^1$, $2^2$, $2^3$'tür. Bir sayı basamak değerlerine ayrıldığında, 100'ün katları (dolayısıyla $2^2$'nin katları), 1000'in katları (dolayısıyla $2^3$'ün katları) otomatik olarak 4'e ve 8'e tam bölünür; geriye yalnızca son 1, son 2, son 3 basamağın etkisi kalır. Bu örüntüye göre, örneğin 16 ($2^4$) ile bölünebilmek için sondan son **4** basamağa, 32 ($2^5$) ile bölünebilmek için sondan son **5** basamağa bakmak gerekir — kural, bölünen sayının 2'nin kaçıncı kuvveti olduğuna göre genelleşir.

**3 ve 9 için (rakamları toplama kuralının ispatı):** Bir sayı basamaklarına ayrıldığında (ör. 3 basamaklı $\overline{abc} = 100a+10b+c$), her basamak değeri "9'un katı + kendisi" biçiminde yazılabilir: $100a = 99a+a$, $10b=9b+b$, $c=c$. 99 ve 9, 9'un (dolayısıyla 3'ün) katı olduğundan bu kısımlar atılabilir; geriye yalnızca $a+b+c$ (rakamlar toplamı) kalır. Sayının 3'e veya 9'a bölümünden kalanı, rakamlar toplamının 3'e veya 9'a bölümünden kalanına eşittir.

**11 için (alternatif toplam kuralının ispatı):** Aynı çözümleme mantığıyla, 10'un kuvvetleri 11'e göre sırayla "+1, -1, +1, -1, ..." fazlalık/eksiklik verir (10 = 11−1, 100 = 99+1, 1000 = 1001−1, ...). 99, 1001, 9999 gibi değerler 11'in katı olduğundan atılır; geriye basamakların **sağdan başlayarak artı-eksi almasıyla oluşan toplam** kalır. Bu yüzden 11 kuralında işaretler mutlaka en sağdaki rakamdan (+) başlar.

[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)

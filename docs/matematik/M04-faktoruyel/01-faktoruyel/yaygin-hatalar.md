# ⚠️ Yaygın Hatalar — faktöriyel

> Kaynak: Öğrencilerin sık yaptığı hatalar ve ÖSYM'nin kurduğu tuzaklar.
> Her madde; hata/tuzak örneği + derin kavrayışla çözümü şeklinde anlatılır.

## 1. Çarpma İçeren İfadeleri Faktöriyel Parantezine Almaya Çalışmak

**Hata:** `7 × 6!` gibi bir ifade, `7!`nin bir parçasıymış gibi
düşünülüp yanlışlıkla parantez veya sadeleştirme işlemine sokulur.

**Neden yanlış:** Parantez alma (ortak çarpan çekme) yalnızca
**toplama/çıkarma** bağlaçlı ifadelerde geçerlidir. `7 × 6!` zaten `7!`e
eşit değildir (`7! = 7 × 6!` olduğu doğrudur ama bu bir çarpım eşitliği
olup toplamalı bir sadeleştirme mantığı gerektirmez).

**Doğru çözüm:** Çarpma içeren ifadelerde doğrudan çarpımı hesapla veya
tanım gereği eşitliği (`7 × 6! = 7!`) kullan; toplama/çıkarma
sadeleştirme tekniklerini burada uygulamaya çalışma.

## 2. Ardışık Faktöriyellerin Toplamında Doğrudan Küçüğü Almak

**Hata:** İki faktöriyelin toplamının (veya farkının) sondan kaç
basamağının `0` olduğu sorulduğunda, faktöriyeller **ardışık** olsa
bile her zaman küçüğün sıfır sayısı cevap olarak verilir.

**Neden yanlış:** Faktöriyeller ardışıksa (`n!` ve `(n-1)!` gibi),
toplam parantezine alındığında (`(n-1)!(n+1)`) açığa çıkan çarpan
(`n+1`) **yeni `5` çarpanları** getirebilir (özellikle `n+1` bir `5`in
katıysa). Bu durumda küçüğün sıfır sayısı **eksik** kalır.

**Doğru çözüm:** Faktöriyeller ardışıksa mutlaka parantez aç, açığa
çıkan çarpanın içindeki ek `5` çarpanlarını da say.

## 3. Asal Olmayan Tabanı Doğrudan Bölmeye Çalışmak

**Hata:** `n!` içinde kaç tane `6` (veya başka bir bileşik sayı)
olduğunu bulmak için, `n` doğrudan `6`ya bölünür ve bölümler toplanır
(asal sayılara bölme mantığıyla aynı şekilde uygulanır).

**Neden yanlış:** `6` asal değildir; `n!`in içinde `6`nın kaç kez tam
sayı çarpanı olarak "üretilebileceği", doğrudan `6`ya bölünerek doğru
bulunamaz — çünkü `6`yı oluşturan `2` ve `3` çarpanları `n!` içinde
farklı sayılarda dağınık halde bulunur.

**Doğru çözüm:** Bileşik tabanı önce asal çarpanlarına ayır (`6=2×3`),
her asal çarpanın `n!` içindeki adedini ayrı ayrı bul, en az bulunan
asalın adedini cevap olarak al.

## 4. Sondan Kaç Basamağının 0 Olduğunu `2`ye Bölerek Bulmaya Çalışmak

**Hata:** Sondan kaç basamağın `0` olduğunu bulmak için `n`, `2`ye
sürekli bölünür (çünkü `10=2×5` ve `2` akla ilk gelen çarpandır).

**Neden yanlış:** `n!` içinde `2` çarpanı her zaman `5` çarpanından
**çok daha fazla** bulunur; sınırlayıcı olan (daha az bulunan) çarpan
`5`tir. `2`ye bölerek bulunan sayı, gerçek sıfır sayısından çok daha
büyük çıkar ve yanlış sonuç verir.

**Doğru çözüm:** Sondan kaç basamağın `0` olduğunu bulmak için her zaman
`n`'i sürekli `5`e böl, bölümleri topla.

## 5. Faktöriyeli Negatif Sayılar İçin de Tanımlıymış Gibi Kullanmak

**Hata:** `(x-5)!` gibi bir ifadede, `x`'e faktöriyeli negatif yapan bir
değer (ör. `x < 5`) verilip işleme devam edilir.

**Neden yanlış:** Faktöriyel yalnızca **doğal sayılarda** (`0, 1, 2,
...`) tanımlıdır; negatif bir sayının faktöriyeli **tanımsızdır**. Bu
tip sorularda `x`'in alabileceği değerler, ifadeyi negatif yapmayacak
şekilde ciddi biçimde kısıtlanır.

**Doğru çözüm:** Faktöriyel içeren her ifadenin **negatif olmaması**
gerektiğini kontrol et; özellikle birbirinin tersi olan iki ifade aynı
anda geçiyorsa (`(x-a)!` ve `(a-x)!`), genellikle yalnızca **tek bir
değer** (ikisini de `0`'a eşitleyen değer) geçerli kalır.

## 6. `0! = 1` Olduğunu Unutup Sıfır Sanmak

**Hata:** Bir ifadede bir faktöriyelden hiçbir çarpan kalmadığında
(örneğin `n!/n!` gibi tam sadeleşen bir durumda), sonucun `0`
olduğu düşünülür.

**Neden yanlış:** Bir faktöriyelden **hiçbir çarpan kalmaması**, `0!`e
denk gelir ve `0! = 1`dir, `0` değil. Bu özellikle "durulan yerde
faktöriyel koy" tekniğinde sık karışan bir noktadır.

**Doğru çözüm:** Sadeleştirme sonunda bir faktöriyelden geriye hiçbir
çarpan kalmıyorsa, oraya `1` yaz (`0!` = `1` olduğu için).

## 7. Ardışık Olmayan Bir Diziyi Faktöriyele Dönüştürmeye Çalışmak

**Hata:** `7 × 5 × 4` gibi aradan bir sayı (`6`) eksik olan bir çarpım
dizisi, "en büyük!/en küçük-1!" kuralı zorlanarak bir faktöriyele
dönüştürülmeye çalışılır.

**Neden yanlış:** Bu dönüşüm kuralı yalnızca dizinin **kesintisiz
ardışık** olduğu durumlarda geçerlidir. Aradan bir sayı eksikse, çarpım
hiçbir faktöriyelin (veya iki faktöriyelin bölümünün) tam karşılığı
olamaz.

**Doğru çözüm:** Faktöriyele dönüştürmeden önce dizinin gerçekten
**ardışık ve azalan** olduğunu doğrula; eksik bir terim varsa doğrudan
çarpım olarak hesapla, faktöriyel kısayoluna güvenme.

## 8. `A! = k × B!` Denkleminde Tek Çözüm Aramak

**Hata:** `A! = 42 × B!` gibi bir denklemde, `42` sayısı yalnızca **tek
bir şekilde** ardışık çarpanlara ayrılır ve tek bir `(A,B)` çifti bulunup
durulur.

**Neden yanlış:** Sabit sayı (`42` gibi), farklı uzunlukta ardışık
çarpan gruplarına (`42×41`, `7×6`, vb.) ayrılabilir; her geçerli ayırma
**ayrı bir çözüm** üretir. Yalnızca ilk bulunan çözümle durmak, olası
diğer değerleri (ve dolayısıyla "değerler toplamı" gibi soruların doğru
cevabını) kaçırmaya sebep olur.

**Doğru çözüm:** Sabit sayıyı ardışık çarpanlara ayırmanın **tüm** olası
yollarını (2'li, 3'lü, 4'lü gruplar vb.) sistematik olarak dene, her
geçerli ayırmayı ayrı bir çözüm olarak say.

[← Konu ana sayfasına dön](index.md) · [Hızlı Tekrar →](hizli-tekrar.md)

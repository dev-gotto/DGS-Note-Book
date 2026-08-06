# 💡 Pratik Bilgiler — asal çarpanlara ayırma

> Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## 1. "Bir Sayıyı Bölen Kaç Sayı Var?" Kısayolu

Büyük bir sayının kaç sayıya bölündüğünü (pozitif bölen sayısını) tek tek
saymak yerine:

1. Sayıyı asal çarpanlarına ayırın, üstlü biçimde yazın.
2. Üsslerin **birer fazlasını** alıp çarpın → pozitif bölen sayısı.
3. Tam sayı (negatifler dahil) bölen sayısı isteniyorsa, bulduğunuz
   sayıyı **2 ile çarpın**.

*Örnek mantık:* $300 = 2^2 \cdot 3^1 \cdot 5^2$ → $(2+1)(1+1)(2+1) = 18$
pozitif bölen.

Bu kısayol, ifadenin **tam sayı/rasyonel sonuç vermesi** gereken
sorularda da işe yarar: "$x$ bir tam sayı olmak üzere $\dfrac{a}{x}$
ifadesi tam sayı ise..." tipi sorularda, $x$'in $a$'yı bölen sayılar
kümesinden geldiği fark edilir edilmez doğrudan pozitif/tam bölen sayısı
formülüne gidilir.

## 2. Asal Olmayan Değişkenlerin Elenmesi

Bir soruda "$B$ asal değildir" gibi ek bir koşul varsa, önce sayının tüm
pozitif bölenlerini (formülle) bulun, sonra bu bölenler kümesinden
**asal olanları çıkarın** (asal çarpanlara ayırırken zaten görünen asal
sayılardır — ayrıca aramaya gerek yoktur). Kalan sayı, koşulu sağlayan
gerçek değer sayısıdır.

## 3. "N'nin Katı Olan Kaç Bölen Var?" Kısayolu

"$N$'nin bölenlerinden kaç tanesi $k$'ya tam bölünür?" tipi sorularda:

1. Önce $N$'yi $k$'ya bölün: $N \div k = m$.
2. $m$'nin pozitif bölen sayısını (formülle) bulun.
3. Bulduğunuz sayı, aynı zamanda $N$'nin $k$'nın katı olan bölen
   sayısıdır.

*Mantık:* $k$'nın katı olan her bölen, $k \times (\text{bir şey})$
biçimindedir; "bir şey" kısmının kaç farklı değer alabileceği,
$N/k$'nın bölen sayısı kadardır.

## 4. Asal Çarpan Sayma Kısayolu ("p'li sayı" ve asal bölen sayısı soruları)

- Bir sayının **asal çarpan (asal bölen) sayısını** sayarken, aynı asal
  sayı birden çok kez (yüksek üslü) geçse bile **bir kez** sayılır. Üsler
  bölen *sayısını* değil, o asal çarpanın "gücünü" gösterir.
- "En büyük asal çarpanı $p$" tipi sorularda, sayının içindeki $p$'den
  büyük bir asal çarpanın **bulunmaması** gerektiğini unutmayın; $p$'den
  küçük asal çarpanlar isteğe bağlı olarak bulunabilir veya
  bulunmayabilir — bu da genelde bir **serbest seçim sayısı**
  (kaç farklı kombinasyon) sorusuna dönüşür.

## 5. Tam Kare Kontrolü

Bir ifadenin (ör. $a^{a}$ gibi kendine üstlü bir ifadenin) tam kare olup
olmadığını sınamak için sayıyı asal çarpanlarına ayırıp **tüm üslerin
çift olup olmadığına** bakın. Tek bir üs bile tek sayıysa ifade tam kare
**değildir** — bunu göstermek için tek bir sayısal karşı örnek (örn.
küçük bir değer denemesi) yeterlidir.

## 6. Farklı Tabanları Ortak Üste Toplama

Bir ifadede aynı asal taban birden fazla yerde geçiyorsa (örn. hem sabit
üslü hem değişken üslü olarak), üslü sayılarda **taban aynıysa üsler
toplanır** kuralını kullanarak önce ifadeleri tek bir üstte birleştirin,
sonra çözüme devam edin.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

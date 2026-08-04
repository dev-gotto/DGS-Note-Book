# 💡 Pratik Bilgiler — bölme

## Bilinmeyenli Bölme Sorularını Çözme Sırası

Harfli/bilinmeyenli bir bölme sorusu geldiğinde izlenecek sabit sıra:

1. **Önce bölmenin sağlamasını yaz:** $A = B \times C + K$.
2. **Sonra bölen > kalan eşitsizliğini yaz:** $B > K$.
3. Bu iki bilgiyi birlikte kullanarak bilinmeyeni (genellikle bölünmesi gereken harf) izole et.

Bu iki adım dışında ekstra bir "kural" aranmaz — bölme sorularının neredeyse tamamı bu iki bilgiyle çözülür.

**Örnek mantık:** $A$'yı bulmak için $B$'ye ihtiyaç varsa ve $B$ doğrudan verilmemişse, bölen>kalan eşitsizliğinden $B$ için bir aralık (ör. "$B$, 11'den küçük") elde edilir; soru "en büyük/en küçük değer" istiyorsa bu aralığın uç değeri kullanılır.

## İki Bölme Denklemi Birlikte Verildiğinde

İki ayrı bölme işlemi aynı harfi (ör. ortak bir $B$) içeriyorsa:

- Her bölme için ayrı ayrı bölen>kalan eşitsizliği yazılır.
- İki eşitsizlik birleştirilerek ortak harfin alabileceği (genelde tek bir) değer bulunur — soruda "en az/en çok" değil de doğrudan bir değer sorulmasının sebebi budur.

## Harfli İfadelerde "Taraf Tarafa Toplama/Çıkarma" Tekniği

İki bölme denklemi, istenen ifadeyi (ör. "$B$'nin $A,C$ türünden eşiti") doğrudan vermiyorsa, iki denklem **taraf tarafa toplanır veya çıkarılır**. Bu, terimlerin birbirini götürüp istenen harfi yalnız bırakmasını sağlar. Bu yöntem her sorunun ilk akla gelen çözümü olmayabilir; alternatifi aşağıdaki "sayı atama" tekniğidir.

## Sayı Atama (Harften Sayıya Geçiş) Tekniği

Bilinmeyen çok, denklemler karışıksa: bölen>kalan koşuluna uyan **keyfi bir sayı** bilinmeyene atanır (genelde işlemi kolaylaştıracak küçük bir değer, sık sık 0 veya 1), sonra zincirleme olarak diğer harfler bu sayı üzerinden hesaplanır. Sonuçta harfli ifade yerine somut sayılarla işlem yapılmış olur. "$X$ türünden ifade" veya "hangisi kesin doğrudur" tarzı sorularda (birden fazla çözümü olabilecek görünen ama tek bir sabit ilişkiye indirgenen sorularda) çok işe yarar.

## Bölme Yapmadan Kalan Bulma

Bir soru "iki sayıyı topla / çıkar / çarp, sonra X'e böl, kalan kaçtır" tarzındaysa:

- Sayıların X'e bölümünden kalanları ayrı ayrı bulunur.
- İşlem (toplama/çıkarma/çarpma) doğrudan **kalanlar üzerinde** yapılır; büyük sayılarla uğraşmaya gerek kalmaz.
- Sonuç, orijinal bölenden büyük çıkarsa tekrar aynı bölene bölünüp son kalan elde edilir.

## Kalan Bulma Sorularında Küçük Sayı Seçme

"$X$ sayısının $n$'e bölümünden kalan $k$'dır" bilgisi verilmiş, $X$'in kendisi sorulmuyor, sadece bir işlemin sonucundaki kalan soruluyorsa: $X$ yerine doğrudan **kalanı** (yani $k$'yı, ya da $k$'ya eşit en küçük pratik sayıyı) yazmak yeterlidir — $X$'in gerçek değerini bulmaya çalışmaya gerek yoktur. Kalanı aynı olan sayılar (ör. 5'e bölümünden kalanı 2 olan 2, 7, 12, 17, ...) bu tarz sorularda birbirinin yerine geçer; en küçüğü seçmek işlemi sadeleştirir.

## Ardışık (Aynı Aralıklı) Değerlerin Toplamı Kısayolu

Bir bilinmeyenin alabileceği değerler eşit aralıklarla artan bir dizi oluşturuyorsa (ör. bölen>kalan koşulundan çıkan "17, 16, 15, ..., 11" gibi bir liste, ya da bölme kuralı sonrası çıkan "1, 4, 7" gibi bir liste), toplamları tek tek eklemek yerine:

$$\text{Toplam} = \text{Ortadaki değer} \times \text{Değer adedi}$$

kısayoluyla hızlıca hesaplanır (dizi tek sayıda terimden oluşuyorsa ortanca terim net biçimde belirlidir).

## Çoklu Kalan Zinciri (Periyodik Kalan) Sorularında Yaklaşım

"$K$'nın 4'e bölümünden kalanı 2, $L$'nin 4'e bölümünden kalanı 3 ise, $K+L$'nin 8'e bölümünden elde edilebilecek **farklı** kalanların toplamı kaçtır" tipi sorularda:

1. $K+L$ tek bir sabit değer değildir; $K$ ve $L$ ayrı ayrı sonsuz sayıda değer alabilir (aynı bölenin katları kadar aralıklarla artan sayılar).
2. Bu yüzden $K+L$ de aynı aralıkla (burada bölenlerin ortak periyoduyla, yani 4'er 4'er) artan sonsuz bir dizi oluşturur.
3. Bu diziyi istenen yeni bölene (burada 8'e) tek tek bölüp elde edilen kalanlara bakılır; kalanlar bir noktadan sonra **tekrar etmeye** başlar.
4. Sadece **farklı** (tekrarsız) kalanlar toplanır — aynı kalan birden fazla kez sayılmaz.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

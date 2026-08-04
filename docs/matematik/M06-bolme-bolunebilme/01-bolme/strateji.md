# 🎯 Soru Çözüm Stratejileri — bölme

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Harfli Bölme Sorusunda Sabit Başlangıç Adımı

Karşına bir bölme (bölünen/bölen içinde harf geçen) sorusu çıktığında
ilk iş her zaman aynıdır: önce **bölmenin sağlamasını** yaz
($A = B \times C + K$), sonra **bölen > kalan** eşitsizliğini yaz.
Bilinmeyeni bulmak için başka bir bilgiye ihtiyaç varmış gibi
hissettiğinde, o eksik bilgi neredeyse her zaman bu iki kuraldan
(çoğunlukla ikincisinden) gelir.

## İki Bölme Denklemi Aynı Harfi Paylaşıyorsa: Aralığı Kesiştir

İki ayrı bölme işlemi ortak bir harf (ör. B) içeriyorsa, her ikisi için
ayrı ayrı bölen>kalan eşitsizliği yazılır; iki eşitsizlik birleştirilip
ortak harfin düşebileceği (genelde tek bir) değer bulunur. "En az/en
çok" değil de doğrudan bir değer sorulmasının sebebi budur.

## Harften Sayıya Geçiş: Küçük ve Elverişli Bir Değer Ata

Bilinmeyen harf sayısı çoksa ya da "X türünden ifade" tarzı bir soru
karışıksa, bölen>kalan koşuluna uyan **küçük** bir sayı (mümkünse `0`
veya `1`, doğal sayı kısıtı varsa `0`'dan başla) bilinmeyene atanır;
zincirleme olarak diğer harfler bu sayı üzerinden hesaplanır. Sayılar
küçük seçildiğinde işlem kısalır ve hata riski azalır.

## Kalan Bulma Sorusunda Sayının Kendisini Değil, Kalanını Kullan

"$A$'nın $n$'e bölümünden kalanı $k$'dır" bilgisi verilip $A$'nın
kendisi değil bir işlemin sonucundaki kalan soruluyorsa, $A$ yerine
doğrudan $k$ yazılır. $A$'yı "$nq+k$" biçiminde açıp şıklara öyle
yerleştirmeye **çalışılmaz** — işlem inanılmaz uzar (bkz. Yaygın
Hatalar #5). Kalanı aynı olan sayılar (ör. 7'ye bölümünden kalanı 2
olan 2, 9, 16, 23, ...) bu tarz sorularda birbirinin yerine geçer; en
küçüğünü seçmek en hızlı yoldur.

## Bölme Yapmadan Kalan Bulma

"İki sayıyı topla/çıkar/çarp, sonra $n$'e böl, kalan kaçtır" tipi
sorularda büyük sayılarla uğraşmaya gerek yok: her sayının $n$'e
bölümünden kalanı ayrı ayrı bulunur, işlem doğrudan **kalanlar
üzerinde** yapılır; sonuç $n$'den büyük çıkarsa tekrar $n$'e bölünüp
son kalan alınır.

## Periyodik (Çoklu) Kalan Sorularında Ortak Periyodu Bul

"$K$'nın $n$'e bölümünden kalanı $k_1$, $L$'nin $n$'e bölümünden kalanı
$k_2$ ise, $K+L$'nin $m$'ye bölümünden elde edilebilecek **farklı**
kalanların toplamı kaçtır" tipi sorularda: $K+L$ tek bir değer
değildir, $n$'er $n$'er artan sonsuz bir dizi oluşturur. Bu diziyi
$m$'ye tek tek bölüp kalanlara bakılır — kalanlar bir noktadan sonra
**tekrar etmeye başlar**; yalnızca tekrarsız (farklı) kalanlar toplanır.

## Basamaklı İfadelerde Bölünürlüğü Parçalara Ayırarak İncele

$AB$ iki basamaklı bir sayı bir asala (ör. 7) tam bölünüyorsa, $AB$'yi
içeren daha büyük bir ifadenin (ör. $ABAB$, $1AB1$) aynı asala
bölünüp bölünmediğini bulmak için ifade, basamak kavramıyla
$AB \times (\text{katsayı}) + (\text{sabit kısım})$ biçiminde ayrıştırılır;
$AB$'li kısmın bölündüğü zaten bilindiğinden, yalnızca sabit kısmın o
asala bölünüp bölünmediğine bakmak yeterlidir.

## Gözden Kaçan İpucunu Arama: Teklik-Çiftlik Kontrolü

Bölen>kalan eşitsizliği tek başına geniş bir aralık veriyorsa ve
soruda kullanılmamış gibi görünen bir sayı/rakam varsa (ör. bir sayının
son basamağının verilmesi), bu neredeyse her zaman bir **teklik-çiftlik**
ya da benzeri bir daraltma ipucudur; aralık bu ek koşulla süzülmeden
cevap tamamlanmış sayılmaz.

---

<a id="ornek-1"></a>
## Örnek 1 — Bölen>Kalan ile En Büyük Değeri Bulma

**Soru:** $x$ pozitif tam sayı ve $x \geq 3$ olmak üzere,
$$A = (x+4) \times 3 + (2x-7)$$
bölme işlemine göre $A$'nın en büyük değeri kaçtır?

**Çözüm:**
- Bu bir bölme sağlaması: bölen $= x+4$, bölüm $=3$, kalan $=2x-7$.
- Bölen>kalan kuralı: $x+4 > 2x-7$ → $11 > x$ → $x < 11$.
- $x$ pozitif tam sayı ve $x \geq 3$ olduğu için en büyük değeri
  $x = 10$'dur.
- $x=10$ için: $A = 3(10+4) + (2\times10-7) = 3\times14 + 13 = 42+13=55$.
- **Sonuç: $A_{\text{max}} = 55$ (C seçeneği).**

<a id="ornek-2"></a>
## Örnek 2 — Ortak Harfi Bölen>Kalan ile Sabitleyip İki Bölmeyi Çözme

**Soru:** $a, b, c$ birer tam sayı olmak üzere,
$$a = 5(b-1) + 2 \qquad c = 5(b+4) + b$$
bölme işlemlerine göre $a + c$ toplamı kaçtır?

**Çözüm:**
- 1. bölme: bölen $=b-1$, kalan $=2$ → bölen>kalan: $b-1 > 2$ → $b>3$.
- 2. bölme: bölen $=5$, kalan $=b$ → bölen>kalan: $5 > b$ → $b<5$.
- İki koşulu birleştir: $3 < b < 5$ → tek çözüm $b=4$.
- $a = 5(4-1)+2 = 15+2 = 17$.
- $c = 5(4+4)+4 = 40+4 = 44$.
- **Sonuç: $a+c = 17+44 = 61$.**

<a id="ornek-3"></a>
## Örnek 3 — Taraf Tarafa Toplayarak Harfi Diğer Harfler Cinsinden Yazma

**Soru:**
$$a = 4B + 1 \qquad c = 5B + 2$$
bölme işlemlerine göre $B$'nin $a, c$ türünden eşiti nedir?

**Çözüm:**
- $a$ ve $c$ ifadelerinde $B$'yi yalnız bırakmak için doğrudan yerine
  koyma yapılamaz (ifadelerde $a$'nın yerine $c$ konamaz); bu yüzden
  iki denklem **taraf tarafa toplanır**.
- $a + c = 9B + 3$ → $B = \dfrac{a+c-3}{9}$.
- **Doğrulama (sayı atama ile):** $B=3$ dersek $a=13$, $c=17$;
  $\dfrac{13+17-3}{9} = \dfrac{27}{9} = 3$ ✓.
- **Sonuç: $B = \dfrac{a+c-3}{9}$ (A seçeneği).**

<a id="ornek-4"></a>
## Örnek 4 — Bağımsız Bölmelerde Sıfır Atayarak Çarpımın Kalanını Bulma

**Soru:** $a, b, c, d$ doğal sayılardır. $a$'yı $12$'ye bölmüşler,
bölüm $b$, kalan $2$'dir. $c$'yi $30$'a bölmüşler, bölüm $d$, kalan
$5$'tir. Buna göre $a \times c$ çarpımının $6$'ya bölümünden kalan
kaçtır?

**Çözüm:**
- İki bölme birbirinden bağımsız (aynı harfler geçmiyor); $b$ ve $d$
  doğal sayı olduğu için en küçük ve en kolay değer olan $0$'ı denemek
  yeterli.
- $b=0$ → $a = 12\times0+2 = 2$.
- $d=0$ → $c = 30\times0+5 = 5$.
- $a \times c = 2 \times 5 = 10$.
- $10$'u $6$'ya böl: $1$ kere var, kalan $4$.
- **Sonuç: kalan $4$ (D seçeneği).**

<a id="ornek-5"></a>
## Örnek 5 — Bölme Yapmadan Kalan Bulma (Zincirleme Bölme)

**Soru:** $X$ ve $Y$ pozitif tam sayılardır. $X$'i $7$'ye bölmüşler,
bölüm $y$, kalan $4$'tür ($X = 7y+4$). $Y$'yi $4$'e bölmüşler, bölüm
$z$, kalan $3$'tür ($y = 4z+3$). Buna göre $X$'in $14$'e bölümünden
kalan nedir?

**Çözüm:**
- $y$'nin değerini $X$'te yerine koy: $X = 7(4z+3)+4$.
- Dağıt: $X = 28z + 21 + 4 = 28z + 25$.
- $28z$ ifadesi $14$'ün tam katıdır ($28 = 14\times2$), yani $14$'e
  bölümünden kalanı etkilemez; kalan sadece $25$'in $14$'e bölümünden
  gelir.
- $25 \div 14$: $1$ kere var, kalan $11$.
- **Kontrol (sayı atama ile):** $z=1$ için $y=7$, $X=53$; $53\div14=3$
  kalan $11$. $z=2$ için $y=11$, $X=81$; $81\div14=5$ kalan $11$.
  Kalan her zaman aynı çıkar (denklik sınıfları mantığı).
- **Sonuç: kalan $11$.**

<a id="ornek-6"></a>
## Örnek 6 — Sayının Yerine Kalanını Kullanarak Tam Bölünmeyi Test Etme

**Soru:** $a$ tam sayısının $7$ ile bölümünden kalan $2$'dir. Buna göre
aşağıdaki ifadelerden hangisi $7$'ye tam bölünür?
A) $a+6$  B) $2a+5$  C) $a^2+1$  D) $a^3-1$  E) $a^2+a+3$

**Çözüm:**
- $a$'yı $7k+2$ biçiminde açıp her şıkka öyle yazmak işlemi çok
  uzatır; bunun yerine $a$'nın **yerine doğrudan kalanı, $2$'yi** yaz.
- A) $2+6=8$ → $7$'ye bölünmez.
- B) $2\times2+5=9$ → bölünmez.
- C) $2^2+1=5$ → bölünmez.
- D) $2^3-1=8-1=7$ → **$7$'ye tam bölünür.**
- E) $2^2+2+3=9$ → bölünmez.
- **Sonuç: D seçeneği.**

<a id="ornek-7"></a>
## Örnek 7 — İki Sayının Kalanını Kullanarak Karışık Bir İfadenin Kalanını Bulma

**Soru:** $x$ sayısının $13$ ile bölümünden kalan $7$, $y$ sayısının
$13$ ile bölümünden kalan $2$'dir. Buna göre $xy + x + y$ ifadesinin
$13$ ile bölümünden kalan kaçtır?

**Çözüm:**
- $x$ yerine $7$, $y$ yerine $2$ yaz (kalan bulma işlemlerinde toplama,
  çıkarma ve çarpmada sayının yerine kalanı kullanılabilir).
- $xy+x+y \to 7\times2 + 7 + 2 = 14+9 = 23$.
- $23$'ü $13$'e böl: $1$ kere var, kalan $10$.
- **Sonuç: kalan $10$.**

<a id="ornek-8"></a>
## Örnek 8 — ÖSYM Tarzı: İki Basamaklı Sayılarla Kurulan Bölmede Taraf Tarafa Toplama

**Soru:** $AB$ ve $BA$ iki basamaklı doğal sayılardır. $AB$'yi
$(A+B)$'ye bölmüşler, bölüm $7$, kalan $3$'tür. $BA$'yı $(A+B)$'ye
bölmüşler, bölüm $3$, kalan $7$'dir. Buna göre $A+B$ toplamı kaçtır?

**Çözüm:**
- Sağlamaları yaz: $AB = 10A+B = 7(A+B)+3$ ve $BA = 10B+A = 3(A+B)+7$.
- İlk denklemi düzenle: $10A+B = 7A+7B+3$ → $3A - 6B = 3$ → $A - 2B = 1$.
- İkinci denklemi düzenle: $10B+A = 3A+3B+7$ → $7B - 2A = 7$.
- $A = 2B+1$'i ikinci denklemde yerine koy: $7B - 2(2B+1) = 7$ →
  $3B = 9$ → $B=3$, dolayısıyla $A = 7$.
- **Kontrol (sayı atama ile):** $A=7, B=3$: $AB=73=7\times10+3$ ✓;
  $BA=37=3\times10+7$ ✓.
- **Sonuç: $A+B = 7+3 = 10$.**

<a id="ornek-9"></a>
## Örnek 9 — Basamak Kavramıyla Birleşik Bölünebilirlik Sorusu

**Soru:** İki basamaklı $AB$ doğal sayısı $7$'ye tam bölünmektedir.
Buna göre aşağıdaki sayılardan hangileri kesinlikle $7$'ye tam
bölünür?
I) $\overline{AB32}$  II) $\overline{ABAB}$  III) $\overline{1AB1}$

**Çözüm:**
- **I)** $\overline{AB32} = 100\times AB + 32$. $100\times AB$, $AB$
  $7$'ye bölündüğü için $7$'ye bölünür; ama $32 \div 7$ kalan $4$
  verir → **toplam $7$'ye bölünmez.**
- **II)** $\overline{ABAB} = 100\times AB + AB = 101\times AB$. $AB$,
  $7$'nin katı olduğundan $101\times AB$ de $7$'nin katıdır →
  **$7$'ye bölünür.**
- **III)** $\overline{1AB1}$'de ortadaki $AB$'yi çıkarırsan geriye
  $1001$ kalır; $AB$'nin basamak değeri (onlar+yüzler) $10\times AB$'dir.
  $\overline{1AB1} = 1001 + 10\times AB$. $10\times AB$, $AB$ $7$'nin
  katı olduğu için $7$'ye bölünür; $1001 = 7\times143$ olduğundan o da
  bölünür → toplam **$7$'ye bölünür.**
- **Sonuç: yalnızca II ve III kesinlikle $7$'ye bölünür (D seçeneği).**

<a id="ornek-10"></a>
## Örnek 10 — Bölen>Kalan Aralığını Ek Bir İpucuyla (Teklik-Çiftlik) Daraltma

**Soru:** $\overline{AB7}$ üç basamaklı, $\overline{KL}$ ve
$\overline{mn}$ iki basamaklı doğal sayılardır. $\overline{AB7}$'yi
$18$'e bölmüşler, bölüm $\overline{KL}$, kalan $\overline{mn}$'dir.
Buna göre $\overline{mn}$'nin alabileceği değerlerin toplamı kaçtır?

**Çözüm:**
- Sağlama: $\overline{AB7} = 18\times\overline{KL} + \overline{mn}$.
- Bölen>kalan: $18 > \overline{mn}$; $\overline{mn}$ iki basamaklı
  olduğu için aday değerler ilk bakışta $10$'dan $17$'ye kadar tüm
  sayılar gibi görünür.
- **Gözden kaçan ipucu:** $\overline{AB7}$'nin son basamağı $7$
  olduğundan $\overline{AB7}$ **tek** bir sayıdır. $18$ çift olduğu
  için $18\times\overline{KL}$ her zaman **çift**tir. Tek olan bir
  sayıdan çift bir sayı çıkarılırsa kalan (yani $\overline{mn}$) da
  **tek** olmak zorundadır.
- Bu ek koşulla $10$–$17$ arası yalnızca tek sayılar kalır: $11, 13,
  15, 17$.
- Toplam: $11+13+15+17 = 56$.
- **Sonuç: $56$.**

<a id="ornek-11"></a>
## Örnek 11 — Periyodik Kalan Zincirinde Farklı Kalanları Bulma

**Soru:** $K$ ve $L$ doğal sayılarının $4$ ile bölümünden kalanları
sırasıyla $2$ ve $3$'tür. Buna göre $K+L$ toplamının $8$ ile
bölümünden elde edilen **farklı** kalanların toplamı kaçtır?

**Çözüm:**
- $K$'nın $4$'e bölümünden kalanı $2$ olduğu için $K \in \{2,6,10,14,
  \dots\}$ (dörder dörder artar); aynı şekilde $L \in \{3,7,11,15,
  \dots\}$.
- $K+L$ tek bir değer değildir; en küçük değer $2+3=5$'ten başlayıp
  **$4$'er $4$'er** artan bir dizi oluşturur: $5, 9, 13, 17, 21, 25,
  \dots$
- Bu dizinin her terimini $8$'e böl: $5\to5$, $9\to1$, $13\to5$,
  $17\to1$, $21\to5$, $25\to1$, ... — kalanlar $5$ ve $1$ arasında
  **tekrar etmeye** başlıyor.
- Farklı (tekrarsız) kalanlar: $\{1, 5\}$.
- **Sonuç: $1+5 = 6$.**

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

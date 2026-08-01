# 💡 Pratik Bilgiler — faktörüyel

> Kaynak: Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## Sadeleştirme Mantığı: Büyüğü Küçüğe Benzet

İki faktöriyel arasında bir işlem (bölme, çarpma, toplama, çıkarma)
olduğunda, temel refleks **büyük faktöriyeli açıp küçük faktöriyele
benzetmektir.** Büyük sayı, kendisinden başlayarak birer birer azalan
çarpanlarla açılır, tam küçük faktöriyele denk gelen yerde durulur ve
oraya faktöriyel işareti konur:

```
20! / 18! → 20! = 20 × 19 × 18! → sadeleştir → 20 × 19 = 380
```

## Kafadan Sadeleştirme (Açmadan Sonuç Çıkarma)

Pratikte iki faktöriyeli tek tek açıp yazmaya gerek yoktur. Büyük
faktöriyelden küçük faktöriyele bölünürken, **geriye küçükten sonraki
çarpanlar kalır:**

```
6! / 3! → 3'ten sonraki çarpanlar: 4 × 5 × 6 = 120
8! / 6! → 6'dan sonraki çarpanlar: 7 × 8 = 56
7! / 4! → 4'ten sonraki çarpanlar: 5 × 6 × 7 = 210
```

## Toplama/Çıkarmalı İfadelerde En Küçüğü Parantezine Al

Faktöriyeller arasında toplama/çıkarma varsa ve sadeleştirmek gerekiyorsa,
**en küçük faktöriyel ortak parantezine alınır.** Parantez içinde
alınan faktöriyelden yalnızca "kendisinden sonraki çarpanlar" kalır;
alınan faktöriyelin kendisinden hiçbir şey kalmazsa yerine `1` yazılır:

```
7! + 6! / 5!  →  5! parantezine al  →  5!(7×6 + 6 + 1) / 5!  →  (42+6+1) = 49
```

(Bu örnekte pay ve payda aynı `5!`yi içerdiği için doğrudan sadeleşir.)

## Pay ve Paydayı Ayrı Ayrı Parantezine Alma

Pay ile paydadaki sayılar arasında **fazla sayıda ara terim** varsa (tüm
terimleri aynı faktöriyelin parantezine almak işlem yükünü artırıyorsa),
pay ve payda **birbirinden bağımsız olarak** kendi içlerindeki en küçük
faktöriyele göre sadeleştirilir, sonra pay/payda ayrı ayrı hesaplanıp
en son birbirine bölünür.

## Faktöriyeller Arasında Çarpma Varsa Parantez Alınmaz

**Kritik kural:** İki faktöriyel arasında **çarpma** işlemi varsa (ör.
`7 × 6!`), bu ifade bir faktöriyel parantezine (`6!` gibi)
**alınamaz** — çünkü zaten `7 × 6!` demek `7!`in bir parçası demek
değildir, doğrudan sadeleştirme mantığı burada geçerli değildir. Parantez
alma yalnızca **toplama/çıkarma** bağlacı olan ifadelerde geçerlidir.

## Çarpmalı-Toplamlı Karışık İfadelerde Ortak Sayıyı Baz Alma

`a! + b! × c` gibi karışık (çarpma + toplama) ifadelerde, ifadelerden
birini **baz alıp** diğerlerini o baza göre sadeleştirerek ortak bir
faktöriyel + kalan sayı formuna indirgemek işlemi hızlandırır (ör.
`7! + 8! + 9!` içinde `7!` ortak faktör olarak çekilip kalan `1 + 8 + 72`
gibi küçük bir toplam bulunur).

## Kesirli İfadelerde Payda Eşitleme

`1/6! + 1/7!` gibi kesirli ifadelerde ortak payda bulmak için, küçük
faktöriyelin **büyük faktöriyele kaç eksiği olduğuna** bakılır (ör. `6!`
ile `7!` arasındaki fark yalnızca çarpan `7`dir); ortak payda doğrudan
büyük faktöriyel olur ve pay buna göre çarpılır.

## Ardışık Azalan Bir Çarpım Dizisini Faktöriyele Dönüştürme (Benzetme)

Ardışık ve **azalarak** giden bir çarpım dizisi (`a × (a-1) × (a-2) ×
...`) her zaman bir faktöriyel biçiminde ifade edilebilir. Dönüştürme
kuralı: **en büyük sayının faktöriyeli, bölü, en küçük sayının bir
eksiğinin faktöriyeli:**

```
8 × 7 × 6 × 5  →  en büyük: 8, en küçük: 5, bir eksiği: 4  →  8! / 4!
```

Ardışıklık **bozulursa** (aradaki bir sayı eksikse) bu dönüşüm
**yapılamaz** — dizi bir faktöriyelin parçası olmaz.

## Denklemde Bilinmeyen Faktöriyeli Bulma (`a! = sayı × b!`)

`a! = k × b!` biçimindeki denklemlerde, sağdaki `k` sayısı **ardışık
azalan çarpanlara** ayrılmaya çalışılır (birden fazla ayırma şekli
denenebilir):

1. `k`'yı `k × (k-1)` gibi kendisinden bir eksiğiyle çarpım şeklinde
   dene.
2. `k`'yı ardışık `3` (veya daha fazla) çarpana ayırmayı dene.
3. Her geçerli ayırma, farklı bir `(a, b)` çözüm çiftine karşılık gelir;
   sorunun istediği toplam/değerler bu çiftlerin hepsi bulunarak elde
   edilir.

## Asal Tabanlı Üs Bulma (`n! = p^x × ...`)

Taban **asal sayıysa**, `n!` içinde o asal sayıdan kaç tane olduğunu
bulmak için `n`, tabana **sürekli bölünür** (bölüm alınır, kalan
atılır) ve bölümler toplanır. Sonuç, o asal sayının `n!` içindeki en
büyük üssünü (`x`'in alabileceği en büyük değeri) verir.

## Asal Olmayan Tabanlı Üs Bulma

Taban **asal değilse** (ör. `6`, `10`, `14`), önce asal çarpanlarına
ayrılır; `n!` içindeki her bir asal çarpanın adedi ayrı ayrı bulunur,
sonra bu adetlerin **en küçüğü** (yani en büyük asal çarpanın adedi)
cevabı verir — çünkü bileşik çarpanı oluşturmak için her asal çarpandan
bir tane gerekir ve en seyrek geçen asal sınırlayıcıdır.

## Sondan Kaç Basamağının 0 Olduğunu Bulma

Bir `n!` sayısının sondan kaç basamağının `0` olduğunu bulmak için,
`n`, sürekli **`5`'e bölünür** (bölüm alınır, kalan atılır) ve bölümler
toplanır. `2` çarpanı her zaman `5`'ten fazla olduğu için sınırlayıcı
olan `5`'tir.

## Toplama/Çarpma/Bölmede Sondan Sıfır Sayısını Birleştirme

İki (ardışık olmayan) faktöriyel içeren işlemlerde sonucun sondan sıfır
sayısı şöyle bulunur:

- **Toplama:** küçüğün sıfır sayısı alınır (küçük belirleyicidir).
- **Çarpma:** iki sayının sıfır sayıları toplanır.
- **Bölme:** iki sayının sıfır sayıları çıkarılır (büyükten küçük
  çıkarılır).

**Dikkat — Ardışık Faktöriyellerde Parantez Gerekir:** Toplanan/çıkarılan
faktöriyeller **ardışıksa** (ör. `24! + 23!`), doğrudan küçüğü almak
**yanlış sonuç verir**, çünkü parantez içinde açığa çıkan yeni bir
çarpan (`24! + 23! = 23!(24+1) = 23! × 25`) **yeni `5` çarpanları**
getirebilir (`25 = 5²`). Bu durumda parantez açılıp içindeki ek `5`
çarpanları da hesaba katılmalıdır.

## Sondan Kaç Basamağının 9 Olduğunu Bulma (`n! - 1` Sorularında)

`n! - 1` gibi bir ifadenin sondan kaç basamağının `9` olduğu sorulursa,
bu doğrudan `n!`in sondan kaç basamağının `0` olduğuna eşittir (bir
sayıdan `1` çıkarınca sondaki `0`lar `9`a döner). Önce `n!`in sıfır
sayısı (5'e bölme yöntemiyle) bulunur, cevap bu sayıdır.

## Değişkenli Faktöriyel İfadelerinde Negatiflik Kısıtı

`(x-a)!` ve `(a-x)!` gibi birbirinin **tersi** olan iki faktöriyel ifade
aynı anda geçiyorsa, ikisinin de **negatif olmaması** gerektiğinden
`x`'in alabileceği değerler ciddi şekilde daralır — genellikle ikisini
de sıfırlayan **tek bir değer** (`x = a`) kalır; diğer tüm değerler
ifadelerden birini negatif yapar ve tanımsızlığa yol açar.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

# 🎯 Soru Çözüm Stratejileri — faktörüyel

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Sadeleştirme Sorularında Büyüğü Küçüğe Açma Stratejisi

İki faktöriyel arasında bölme/çarpma/toplama/çıkarma varsa, büyük olanı
küçük olana göre aç, sadeleştir. Kafadan yapmak için: büyük faktöriyelden
küçük faktöriyele bölerken geriye **küçükten sonraki çarpanlar** kalır.

## Toplamalı/Çıkarmalı İfadelerde En Küçüğü Parantezine Alma Stratejisi

Faktöriyeller arasında `+`/`-` varsa, en küçük faktöriyeli ortak
parantezine al; parantez içinde her terimden yalnızca "kendisinden
sonraki çarpanlar" kalır (hiçbir şey kalmıyorsa `1` yaz).

## Pay/Payda Ayrı Sadeleştirme Stratejisi

Aradaki terim sayısı fazlaysa (tek parantezle sadeleştirmek karmaşık
oluyorsa), pay ve paydayı **ayrı ayrı** kendi en küçük faktöriyellerine
göre sadeleştir, sonra ikisini birbirine böl.

## Ardışık Azalan Diziyi Faktöriyele Çevirme Stratejisi

`a × (a-1) × (a-2) × ...` biçiminde ardışık azalan bir çarpım görürsen,
bunu **en büyük sayının faktöriyeli / en küçük sayının bir eksiğinin
faktöriyeli** olarak yaz.

## `a! = k × b!` Denklemlerini Çözme Stratejisi

`k` sabit sayısını ardışık azalan çarpanlara ayırmayı dene (birden fazla
ayırma biçimi olabilir); her geçerli ayırma bir `(a,b)` çözüm çiftidir.

## Asal Çarpan Sayısı Bulma Stratejisi

Taban asalsa `n`'i tabana sürekli böl, bölümleri topla. Taban asal
değilse önce asal çarpanlarına ayır, en büyük asal çarpana göre böl (en
az bulunan asal sınırlayıcıdır).

## Sondan Sıfır Sayısı Bulma Stratejisi

`n`'i sürekli `5`'e böl, bölümleri topla. Toplama işleminde küçüğü al,
çarpmada topla, bölmede çıkar; ardışık faktöriyellerde parantez aç ve
yeni oluşan `5` çarpanlarını da say.

---

<a id="ornek-1"></a>
## Örnek 1 — Basit Sadeleştirme

**Soru:** `7! / 6!` işleminin sonucu kaçtır?

**Çözüm:**
- `7!`, `6!`'ye göre açılır: `7! = 7 × 6!`.
- Sadeleştirilince yalnızca `7` kalır.
- **Sonuç: `7`.**

<a id="ornek-2"></a>
## Örnek 2 — Büyük Aradaki Sadeleştirme

**Soru:** `20! / 18!` işleminin sonucu kaçtır?

**Çözüm:**
- `20!`, `18!`ye göre açılır: `20! = 20 × 19 × 18!`.
- Sadeleştirilince `20 × 19 = 380` kalır.
- **Sonuç: `380`.**

<a id="ornek-3"></a>
## Örnek 3 — Toplamalı İfadede Parantez Alma

**Soru:** `(7! + 6!) / 5!` işleminin sonucu kaçtır?

**Çözüm:**
- En küçük faktöriyel `5!`; pay `5!` parantezine alınır.
- `7!`den `5!` atılınca kalan: `6 × 7 = 42`.
- `6!`den `5!` atılınca kalan: `6`.
- Pay: `5!(42 + 6) = 5! × 48`.
- `5!` sadeleşir, geriye `48` kalır.
- **Sonuç: `48`.**

<a id="ornek-4"></a>
## Örnek 4 — Üç Terimli Karışık Kesir

**Soru:** `(11! - 10!) / (9! + 8!)` işleminin sonucu kaçtır?

**Çözüm:**
- Pay için en küçük `10!`: `11! - 10! = 10!(11 - 1) = 10! × 10`.
- Payda için en küçük `8!`: `9! + 8! = 8!(9 + 1) = 8! × 10`.
- `10! / 8! = 9 × 10 = 90`; ifade `(10! × 10) / (8! × 10)` → `10`lar
  sadeleşir, geriye `10!/8! = 90` kalır.
- **Sonuç: `90`.**

<a id="ornek-5"></a>
## Örnek 5 — Pay ve Paydayı Ayrı Ayrı Sadeleştirme

**Soru:** `(7! - 6! + 5!) / (4! - 3! + 2!)` işleminin sonucu kaçtır?

**Çözüm:**
- Pay: en küçük `5!` parantezine alınır. `7!`den kalan `6×7=42`,
  `6!`den kalan `6`, `5!`den kalan `1` → pay `5!(42 - 6 + 1) = 5! × 37`.
- Payda: en küçük `2!` parantezine alınır. `4!`den kalan `3×4=12`,
  `3!`den kalan `3`, `2!`den kalan `1` → payda `2!(12 - 3 + 1) = 2! × 10`.
- Pay ve payda, kalan faktöriyeller cinsinden birbirine bölünür:
  `5!/2! = 3 × 4 × 5 = 60`.
- Sonuç: `(60 × 37) / 10 = 2220 / 10 = 222`.
- **Sonuç: `222`.** (Yöntem: pay ve paydayı ayrı ayrı kendi en küçük
  faktöriyellerine göre sadeleştir, sonra kalan sayıları birbirine böl.)

<a id="ornek-6"></a>
## Örnek 6 — Payda Eşitleme (Kesirli İfade)

**Soru:** `1/6! + 1/7!` toplamı, ortak payda ile nasıl ifade edilir?

**Çözüm:**
- `6!` ile `7!` arasındaki fark yalnızca çarpan `7`dir (`7! = 7 × 6!`).
- Ortak payda doğrudan `7!` olur: `1/6! = 7/7!`.
- Toplam: `7/7! + 1/7! = 8/7!`.
- **Sonuç: `8/7!`.**

<a id="ornek-7"></a>
## Örnek 7 — Ardışık Azalan Diziyi Faktöriyele Çevirme

**Soru:** `8 × 7 × 6 × 5` çarpımı hangi iki faktöriyelin bölümüne eşittir?

**Çözüm:**
- Dizi ardışık ve azalarak gidiyor: en büyük sayı `8`, en küçük sayı
  `5`; en küçüğün bir eksiği `4`.
- Kural: en büyük sayının faktöriyeli / en küçük sayının bir eksiğinin
  faktöriyeli.
- **Sonuç: `8! / 4!`.**

<a id="ornek-8"></a>
## Örnek 8 — Ardışık Azalan Diziyi Faktöriyele Çevirme (İkinci Örnek)

**Soru:** `12 × 11 × 10 × 9 × 8` çarpımı hangi iki faktöriyelin bölümüne
eşittir?

**Çözüm:**
- En büyük sayı `12`, en küçük sayı `8`; en küçüğün bir eksiği `7`.
- **Sonuç: `12! / 7!`.**

<a id="ornek-9"></a>
## Örnek 9 — `a! = k × b!` Denklemi

**Soru:** `n × (n-1) = 30 × 4!` eşitliği sağlandığına göre `n` kaçtır?

**Çözüm:**
- Sol taraf `n × (n-1)`, ardışık iki azalan çarpan; sağ tarafın da bir
  faktöriyelin açılımı olması gerekir.
- `30`, ardışık çarpanlara ayrılır: `30 = 6 × 5`, böylece sağ taraf
  `6 × 5 × 4! ` olur — bu `6!`nin açılımıdır.
- Sol taraf `n × (n-1)` de aynı biçimde `n!`nin açılımı olmalı;
  `n! = 6!` olduğundan `n = 6`.
- **Sonuç: `n = 6`.**

<a id="ornek-10"></a>
## Örnek 10 — `A! = 42 × B!` Denklemi (Birden Fazla Çözüm)

**Soru:** `A! = 42 × B!` olduğuna göre `A`'nın alabileceği değerler
toplamı kaçtır?

**Çözüm:**
- `42`, ardışık azalan çarpanlara farklı biçimlerde ayrılabilir:
  - `42 = 42 × 41 / 41` biçiminde düşünülürse `42 × 41!` → bu `42!`nin
    açılımı olur (`B = 41`), o zaman `A = 42`.
  - `42 = 7 × 6` biçiminde düşünülürse `7 × 6 × 5!` → bu `7!`nin
    açılımı olur (`B = 5`), o zaman `A = 7`.
  - `42`'nin ardışık **3** çarpana ayrılması (ör. `42 = 7 × 6 × 1`
    biçiminde denenirse) ardışıklık koşulunu sağlamadığından geçersizdir.
- Geçerli iki değer: `A = 42` ve `A = 7`.
- **Sonuç: `42 + 7 = 49`.**

<a id="ornek-11"></a>
## Örnek 11 — `P! / R! = 5!` Denklemi (Çok Çözümlü)

**Soru:** `P` ve `R` doğal sayılar olmak üzere `P! / R! = 5!` eşitliği
sağlanmaktadır. Buna göre `R`'nin alabileceği değerler toplamı kaçtır?

**Çözüm:**
- `5! = 120`. `P!/R! = 120` içler dışlar yapılırsa `P! = 120 × R!`.
- `120`'yi ardışık azalan çarpanlara ayırmanın olası yolları:
  - `120 = 120 × 119 / 119` biçiminde: `P! = 120 × 119!` → `P!` doğrudan
    `120!`nin açılımı, `R = 119`.
  - `120`, ardışık **2** çarpan olarak yazılamaz (`120`e en yakın
    ardışık ikili `10×12` çarpımı vermiyor).
  - `120 = 6 × 5 × 4` biçiminde: ardışık `3` çarpan, `R = 3`.
  - `120 = 5 × 4 × 3 × 2` biçiminde: ardışık `4` çarpan, `R = 1`.
  - `120 = 5 × 4 × 3 × 2 × 1` biçiminde: ardışık `5` çarpan, `R = 0`.
- Toplamda `R`, `4` farklı değer alabiliyor: `119, 3, 1, 0`.
- **Sonuç: `119 + 3 + 1 + 0 = 123`.**

<a id="ornek-12"></a>
## Örnek 12 — Asal Tabanda Üs Bulma (`9!` İçindeki `2` Çarpanı)

**Soru:** `9! = 2^a × b` olduğuna göre (`b` tek sayı), `a`'nın
alabileceği en büyük değer kaçtır?

**Çözüm:**
- Taban `2` asal sayı olduğundan `9`, sürekli `2`ye bölünür:
  `9 / 2 = 4` (bölüm), `4 / 2 = 2`, `2 / 2 = 1`.
- Bölümler toplanır: `4 + 2 + 1 = 7`.
- **Sonuç: `a`'nın en büyük değeri `7`.**

<a id="ornek-13"></a>
## Örnek 13 — Asal Olmayan Tabanda Üs Bulma (`9!` İçindeki `6` Çarpanı)

**Soru:** `9!` içinde en fazla kaç tane `6` çarpanı vardır?

**Çözüm:**
- `6` asal değildir (`6 = 2 × 3`), önce asal çarpanlarına ayrılır.
- `9!` içindeki `2` sayısı `7` (önceki örnekten), `3` sayısı ise `9`'u
  sürekli `3`e bölerek bulunur: `9/3 = 3`, `3/3 = 1`, toplam `3 + 1 = 4`.
- `6` çarpanı oluşturmak için her seferinde bir `2` ve bir `3` gerekir;
  sınırlayıcı olan (daha az bulunan) `3`'lerin sayısıdır.
- **Sonuç: `9!` içinde en fazla `4` tane `6` çarpanı vardır.**

<a id="ornek-14"></a>
## Örnek 14 — Kombine Soru: `X`, `Y`, `Z` Üslerini Bulma

**Soru:** `X` ve `Y` pozitif tam sayılardır. `9! = 2^X × 3^Y × Z`
olduğuna göre `Z` en az kaçtır?

**Çözüm:**
- `9!` sürekli `2`ye bölünerek `X` (en büyük değer) bulunur: `7`.
- `9!` sürekli `3`e bölünerek `Y` (en büyük değer) bulunur: `4`.
- `Z`'nin en az olması için `2` ve `3` çarpanlarının **tamamı** `X` ve
  `Y`'ye aktarılır; geriye `9!`in içindeki diğer asal çarpanlar
  (`5` ve `7`) kalır.
- **Sonuç: `Z = 5 × 7 = 35`.**

<a id="ornek-15"></a>
## Örnek 15 — Sondan Kaç Basamağının 0 Olduğu

**Soru:** `72!` sayısının sondan kaç basamağı `0`'dır?

**Çözüm:**
- `72`, sürekli `5`e bölünür: `72/5 = 14` (bölüm), `14/5 = 2` (bölüm).
- Bölümler toplanır: `14 + 2 = 16`.
- **Sonuç: `16` basamak `0`'dır.**

<a id="ornek-16"></a>
## Örnek 16 — `n! - 1` Sayısının Sondan Kaç Basamağının 9 Olduğu

**Soru:** `124! - 1` sayısının sondan kaç basamağı `9`'dur?

**Çözüm:**
- Önce `124!`in sondan kaç basamağının `0` olduğu bulunur: `124/5 = 24`
  (bölüm), `24/5 = 4` (bölüm); toplam `24 + 4 = 28`.
- Bir sayıdan `1` çıkarılınca sondaki `0`lar `9`a dönüşür; dolayısıyla
  `124! - 1` sayısının da sondan `28` basamağı `9`dur.
- **Sonuç: `28`.**

<a id="ornek-17"></a>
## Örnek 17 — Toplamada Küçüğü Alma (Ardışık Olmayan)

**Soru:** `37! + 71!` toplamının sondan kaç basamağı `0`'dır?

**Çözüm:**
- Toplamada belirleyici olan **küçük** faktöriyeldir (`37!`).
- `37`, sürekli `5`e bölünür: `37/5 = 7`, `7/5 = 1`; toplam `7 + 1 = 8`.
- **Sonuç: `8` basamak `0`'dır.**

<a id="ornek-18"></a>
## Örnek 18 — Çarpma ve Bölmede Sıfır Sayısını Birleştirme

**Soru:** `53! × 12!` çarpımının ve `62! / 27!` bölümünün sondan kaç
basamağının `0` olduğunu bulunuz.

**Çözüm (çarpma):**
- `53!`in sıfır sayısı: `53/5=10`, `10/5=2` → toplam `12`.
- `12!`in sıfır sayısı: `12/5=2` → toplam `2`.
- Çarpmada sıfır sayıları **toplanır**: `12 + 2 = 14`.
- **Sonuç (çarpma): `14` basamak `0`'dır.**

**Çözüm (bölme):**
- `62!`in sıfır sayısı: `62/5=12`, `12/5=2` → toplam `14`.
- `27!`in sıfır sayısı: `27/5=5`, `5/5=1` → toplam `6`.
- Bölmede sıfır sayıları **çıkarılır**: `14 - 6 = 8`.
- **Sonuç (bölme): `8` basamak `0`'dır.**

<a id="ornek-19"></a>
## Örnek 19 — Ardışık Faktöriyellerin Toplamında Parantez Zorunluluğu

**Soru:** `24! + 23!` toplamının sondan kaç basamağı `0`'dır?

**Çözüm:**
- `24!` ile `23!` **ardışıktır**; doğrudan küçüğü (`23!`) almak
  **yanlış** olur, çünkü parantez açıldığında yeni bir `5` çarpanı
  ortaya çıkabilir.
- Parantez alınır: `24! + 23! = 23!(24 + 1) = 23! × 25`.
- `23!`in sıfır sayısı (yani içindeki `5` çarpanı sayısı): `23/5 = 4`
  (bölüm) → `4`.
- `25 = 5²`, kendisi **2 tane** ek `5` çarpanı getirir.
- Toplam `5` çarpanı: `4 + 2 = 6`.
- **Sonuç: `6` basamak `0`'dır.**

<a id="ornek-20"></a>
## Örnek 20 — Toplamada Ardışıklık Testi ve Bölme Zinciri

**Soru:** `(72! + 42!) / (89! - 27!)` ifadesindeki pay ve paydanın her
biri için sondan kaç basamağının `0` olduğunu ayrı ayrı bulunuz (pay ve
payda ardışık değildir).

**Çözüm:**
- Pay `72! + 42!`: ardışık değil, küçük olan `42!` belirleyici.
  `42/5=8`, `8/5=1` → toplam `9`. **Pay: `9` basamak `0`.**
- Payda `89! - 27!`: ardışık değil, küçük olan `27!` belirleyici.
  `27/5=5`, `5/5=1` → toplam `6`. **Payda: `6` basamak `0`.**
- Bölmede sıfır sayıları çıkarılır: `9 - 6 = 3`.
- **Sonuç: Bölümün sondan `3` basamağı `0`'dır.**

<a id="ornek-21"></a>
## Örnek 21 — Faktöriyel Karelerinin Sıralanması

**Soru:** `x = (9! - 8!)² / 8!²`, `y = (8! + 7!)² / 7!²`,
`z = (7! + 6!)² / 6!²` olduğuna göre `x`, `y`, `z` sayılarını
küçükten büyüğe sıralayınız.

**Çözüm:**
- Her ifade `(a! ± b!)² / b!²` biçiminde: ortak `b!` çekilip
  sadeleştirildiğinde ifade doğrudan `(kalan sabit sayı)²`ye indirgenir
  — kareler zaten ortak olduğu için ayrıca hesaba katılmaz.
- `x`: `9! - 8! = 8!(9-1) = 8! × 8` → sadeleşince `x = 8² = 64`.
- `y`: `8! + 7! = 7!(8+1) = 7! × 9` → sadeleşince `y = 9² = 81`.
- `z`: `7! + 6! = 6!(7+1) = 6! × 8` → sadeleşince `z = 8² = 64`.
- **Sonuç: `x = z = 64`, `y = 81`; sıralama `x = z < y`.**

<a id="ornek-22"></a>
## Örnek 22 — İşlenmiş Sayıları Faktöriyele Çevirme (Proje/Öğrenci Sorusu)

**Soru:** Bir projede birinci bölgeden `8` il × `7` ilçe × `4` okul ×
`3` öğrenci, ikinci bölgeden `16` il × `3` ilçe × `7` okul × `3`
öğrenci seçiliyor. Toplam öğrenci sayısını, çarpanları faktöriyele
dönüştürerek bulunuz.

**Çözüm:**
- Birinci bölge çarpımı: `8 × 7 × 4 × 3 = 672`. Ortak çarpanlar (`7` ve
  `3`) parantezine alınır: `7 × 3 × (8 × 4) = 21 × 32`.
- İkinci bölge çarpımı: `16 × 3 × 7 × 3 = 1008`; aynı ortak çarpanlarla
  düzenlenir: `7 × 3 × (16 × 3) = 21 × 48`.
- Ortak çarpan `21` her iki bölgede de bulunduğundan parantezine alınır:
  toplam `21 × (32 + 48) = 21 × 80 = 1680`.
- `1680`, ardışık azalan dizi `8 × 7 × 6 × 5`e eşittir (`8 × 7 × 6 × 5 =
  1680`), yani `8! / 4!` şeklinde de ifade edilebilir.
- **Sonuç:** Toplam öğrenci sayısı `1680`'dir (`8!/4!` biçiminde de
  yazılabilir).

<a id="ornek-23"></a>
## Örnek 23 — En Çok Fark Sorusu (`T`, `P`, `R` Demir Blokları)

**Soru:** Üç demir bloğunun ağırlıkları `T = B! × 7!` (en hafif),
`P = 6! × 8!` (orta), `R = A! × 8!` (en ağır) biçiminde veriliyor
(`T < P < R`). Buna göre `B - A` farkı en çok kaçtır?

**Çözüm:**
- Her üç ifade de `7!` cinsinden yazılır (`8! = 8 × 7!`):
  `T = B! × 7!`, `P = 6! × 8 × 7!`, `R = A! × 8 × 7!`.
- `7!` ortak olduğundan sadeleştirilir, karşılaştırma
  `B! < 6! × 8 < A!` üzerinden yürür (payda `T<P` kısmında `7!`
  sadeleşince `B! < 6!×8`, `P<R` kısmında ise `8` çarpanı ortak olduğundan
  doğrudan `6! < A!` kalır).
- `6! × 8 = 5760`, bu değer `7! = 5040` ile `8! = 40320` arasındadır.
  `B! < 5760` koşulunu sağlayan en büyük faktöriyel `7! = 5040`
  olduğundan `B`'nin en büyük değeri `7`dir.
- `6! < A!` koşulunu sağlayan en küçük faktöriyel `7!` olduğundan
  `A`'nın en küçük değeri de `7`dir.
- **Sonuç: `B - A` farkı en çok `7 - 7 = 0` olabilir.**

<a id="ornek-24"></a>
## Örnek 24 — Dairelere Ardışık Rakam Yazma (Faktöriyel Oluşturma)

**Soru:** `0`'dan `9`'a kadar rakamlar, hem yukarıdan aşağıya `4`
dairenin içine hem de soldan sağa `3` dairenin içine ardışık şekilde
yazılacak; her iki yöndeki çarpım da bir faktöriyele eşit olmalıdır.
Kesişimdeki ortak sayıdan başlayarak `a` (yukarıdan aşağı ilk sayı) ve
`b` (soldan sağa son sayı) belirleniyor. Buna göre `a + b` toplamı
kaçtır?

**Çözüm:**
- İlk denenen grup — yukarıdan aşağı `1,2,3,4` (çarpım `24 = 4!`) —
  soldan sağa yönde kesişim sayısından (`4`) devam eden ardışık üçlü
  `3,4,5` çarpımı `60` verir; `60` bir faktöriyele eşit olmadığından bu
  grup **elenir.**
- İkinci grup — yukarıdan aşağı `2,3,4,5` (çarpım `120 = 5!`) — soldan
  sağa yönde kesişim sayısından (`5`) devam eden ardışık üçlü `4,5,6`
  çarpımı da `120 = 5!` verir. İki yön de **aynı faktöriyele** eşit
  olduğundan bu grup **geçerlidir.**
- Başka bir kaydırma (`3,4,5,6` dikey / `5,6,7` yatay) denendiğinde
  `5×6×7=210` bir faktöriyele denk gelmediğinden elenir; çözüm tektir.
- Bu tek geçerli çözümde dikey grubun ilk sayısı `4`, yatay grubun son
  sayısı `3` olarak belirlenir.
- **Sonuç: `a + b = 4 + 3 = 7`.**

<a id="ornek-25"></a>
## Örnek 25 — İki Şart Birden: Asal Çarpan Sayısı + 5 Çarpanı Sayısı

**Soru:** `n!` sayısının `9` farklı asal çarpanı vardır ve içindeki `5`
çarpanlarının sayısı `6`dır. Buna göre `n`'in alabileceği değerler
toplamı kaçtır?

**Çözüm:**
- **1. şart:** `9` farklı asal çarpan bulunması için `n!`in içinde
  küçükten büyüğe `9`. asal sayıya (`2,3,5,7,11,13,17,19,23`) kadar
  ulaşılmalı, yani `n ≥ 23` olmalı. `29` bir sonraki asal sayı olduğundan
  `n ≤ 28` olmalı (aksi halde `10`. asal çarpan eklenir). Bu şart tek
  başına `n`'i `23`–`28` arasına sınırlar.
- **2. şart:** `5` çarpanlarının sayısının `6` olması için `n`, sürekli
  `5`e bölündüğünde bölümler toplamı `6` vermeli. `n = 23` ve `n = 24`
  için `5` çarpanı sayısı henüz `5`tir (`23/5=4`, yetersiz); `n = 25`ten
  itibaren (`25 = 5²` yeni bir `5` çarpanı ekler) toplam `6`ya çıkar.
- İki şartı birden sağlayan değerler: `25, 26, 27, 28`.
- **Sonuç: `25 + 26 + 27 + 28 = 106`.**

<a id="ornek-26"></a>
## Örnek 26 — Negatif Faktöriyel Kısıtı (Tersine Değişkenler)

**Soru:** `x` pozitif tam sayı olmak üzere `(x-5)! / (5-x)!` ifadesi
tanımlıysa, `x` kaç olmalıdır?

**Çözüm:**
- `(x-5)!` ve `(5-x)!` birbirinin tersidir; faktöriyel negatif sayılarda
  tanımlı olmadığından **ikisinin de aynı anda negatif olmaması**
  gerekir.
- `x` için `6` ve üzeri denenirse `5-x` negatif olur (tanımsız);
  `4` ve altı denenirse `x-5` negatif olur (tanımsız).
- Geriye kalan tek değer, ikisini birden `0`'a eşitleyen `x = 5`'tir
  (`0! = 1`, tanımlıdır).
- **Sonuç: `x = 5`.**

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

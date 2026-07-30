# 🎯 Soru Çözüm Stratejileri — ardışık sayılar

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Fark Bilgisi Verilince Harflerle Uğraşma, Farkı Doğrudan Kullan

İki ayrı ardışık grubun (ör. iki farklı ardışık tek sayı dizisi) belirli
üyeleri arasındaki fark verildiğinde, her terimi `x`, `x+2`, `y`, `y+2`
gibi ayrı ayrı yazıp uzun bir denklem kurmak yerine, istenen farkı
doğrudan verilen sabit farkın cinsinden ifade et. Bu, çözüm süresini
ciddi biçimde kısaltır.

## Fark Sorularında Sayı Yapıştırma Stratejisi

Soru yalnızca **farkla** ilgiliyse (harflerin kendi değerleriyle değil),
harflerin yerine dizinin türüne uygun küçük sayılar (`2, 4, 6` gibi)
yerleştirip işlemi doğrudan sonuçlandır — fark sabit olduğu için hangi
üçlüyü seçtiğin sonucu değiştirmez.

## Tek Terim Sayılı Toplamlarda Ortadaki Sayıdan Yürü

Terim sayısı tek olan bir grubun toplamı verildiğinde, sayıları tek tek
`x`li ifadeler hâlinde yazıp toplamak yerine: toplamı terim sayısına böl
→ ortadaki sayıyı bul → istenen terime (en küçük/en büyük/N. sayı) oradan
adım adım ilerle.

## Toplamdan Terim Çıkarma / Terim Bulma Stratejisi

Bir grubun tamamının toplamı biliniyor, ama gruptan birkaç terim
çıkarıldıktan sonraki (kalan) toplam veriliyorsa: **tüm grubun standart
toplamından kalan toplamı çıkararak** çıkarılan terimlerin toplamını
bul, sonra bu küçük toplamı aynı mantıkla (terim sayısı × ortadaki sayı)
çöz.

## Hata Bulma Stratejisi (Artı Yerine Eksi)

Toplama işleminde bir terimin önüne yanlışlıkla eksi konduğu
belirtildiğinde, doğru (standart) toplamla yanlış sonuç arasındaki farkı
`2`ye böl — bu, yanlışlıkla eksi konan terimi doğrudan verir.

## Çarpımsal Terimli Serilerde Sabit Çarpanı Silme Stratejisi

Bir terimin yalnızca bir çarpanı belirli bir miktar artırıldığında,
değişmeyen çarpanları zihinsel olarak sil, geriye kalan (değişen)
çarpanlarla oluşan yeni ardışık diziyi topla, bulduğun toplamı artış
miktarıyla çarp.

---

<a id="ornek-1"></a>
## Örnek 1 — Ev Numaraları: Fark Bilgisiyle Kısa Yol

**Soru:** Bir sokakta, yolun üst tarafındaki evler ardışık tek
sayılarla, alt tarafındaki evler ardışık çift sayılarla
numaralandırılmıştır (numaralar soldan sağa doğru artmaktadır). `A` ve
`C` evleri üst sıradadır ve `A - C` farkı `23`'tür. `B` ve `D` evleri
alt sıradadır. Buna göre `B - D` farkı kaçtır?

**Çözüm (kısa yol):**
- Üstteki (tek sayılı) evler kendi içinde ardışık, alttaki (çift sayılı)
  evler de kendi içinde ardışıktır — fark her iki sıra için de sabittir.
- `A - C = 23` bilgisi zaten üst sıranın sabit farkını temsil eder;
  `x`, `x+2` gibi harflerle yeniden kurmaya gerek yoktur.
- Alt sıradaki evler de aynı mantıkla ardışık olduğundan, karşılıklı
  evler arasındaki ilişki üst sıradakiyle **aynı kalıptadır**: üst sırada
  `A`'dan `C`'ye giderken kaç ev atlanıyorsa alt sırada `B`'den `D`'ye
  giderken de aynı sayıda ev atlanır, dolayısıyla iki sıranın farkları
  arasında sabit bir kaymayla ilişki kurulabilir.
- Bu ilişki kurulduğunda `B - D = 25` bulunur.
- **Sonuç: `B - D = 25`.** (Harfleri `x`, `x+2`, `y`, `y+2` şeklinde açıp
  uzun denklem kurmak da aynı sonucu verir, ama gereksiz derecede
  uzundur — bu yüzden "yol değil" olarak nitelenir.)

<a id="ornek-2"></a>
## Örnek 2 — Fark Bilgisiyle Denklem Kurma

**Soru:** `a, b, c` küçükten büyüğe sıralı ardışık tek sayılardır.
`4b = 9(c - a)` olduğuna göre `a + b + c` toplamı kaçtır?

**Çözüm:**
- `a, b, c` ardışık tek sayılar olduğundan ikişer ikişer artar:
  `c - a = 4`.
- Bu bilgi doğrudan denklemde yerine konur: `4b = 9 × 4 = 36`.
- Buradan `b = 9`.
- `b` bulunduğunda tüm dizi bulunmuş olur: ardışık tek sayılarda bir
  öncesi `2` az, bir sonrası `2` fazladır → `a = 7`, `c = 11`.
- **Sonuç: `a + b + c = 7 + 9 + 11 = 27`.**

<a id="ornek-3"></a>
## Örnek 3 — Harf İfadeleriyle Verilen Ardışık Sayılar

**Soru:** `m, m+n, 2m` sayıları küçükten büyüğe sıralanmış, ardışık 3
çift sayıdır. Buna göre `m × n` kaçtır?

**Çözüm:**
- Ardışık çift sayılarda artış miktarı `2`'dir: `(m+n) - m = 2` ya da
  `2m - (m+n) = 2` ya da `2m - m = 4` (ilk terimden son terime iki adım).
- En basit ilişkiden gidilir: `2m - m = 4` olduğundan doğrudan `m = 4`.
- `(m+n) - m = 2` ilişkisinden `n = 2`.
- **Sonuç: `m × n = 4 × 2 = 8`.**

<a id="ornek-4"></a>
## Örnek 4 — "İkili Ardışık Sayı" Tanım Sorusu

**Soru:** Hem ardışık iki pozitif tam sayının hem de ardışık üç pozitif
tam sayının toplamı biçiminde yazılabilen sayılara **"ikili ardışık
sayı"** denir. Buna göre:

  I. `39`
  II. `240`
  III. `693`

sayılarından hangileri ikili ardışıktır?

**Çözüm:**
- **Kural 1:** Ardışık iki sayının toplamı her zaman **tektir.** `240`
  çift olduğundan bu koşulu sağlayamaz — **II elenir.**
- **Kural 2:** Ardışık üç sayının toplamı her zaman **3'ün katıdır.**
  - `39`: hem tek hem `3`'ün katı (`3+9=12`, `12` de `3`'ün katı) →
    uygun. Doğrulama: `19 + 20 = 39` (ardışık iki) ve
    `12 + 13 + 14 = 39` (ardışık üç) — ikisi de sağlanıyor.
  - `693`: rakamları toplamı `6+9+3=18`, `3`'ün katı, ve `693` tek sayı
    → her iki koşulu da sağlıyor.
- **Sonuç: I ve III (`39` ve `693`) ikili ardışık sayıdır.**

<a id="ornek-5"></a>
## Örnek 5 — Toplamdan En Küçük Terimi Bulma (Tek Terim Sayısı)

**Soru:** Ardışık 7 tek sayının toplamı `105` ise, bu sayıların en
küçüğü kaçtır?

**Çözüm:**
- Terim sayısı `7` (tek) → gerçek bir ortadaki sayı vardır.
- Ortadaki sayı: `105 / 7 = 15`.
- `7` terimde ortadakinden sola doğru `3` adım vardır; tek sayılarda
  adım başına `2` azalır: `15 - 2 - 2 - 2 = 9`.
- **Sonuç: En küçük sayı `9`'dur.**

<a id="ornek-6"></a>
## Örnek 6 — Toplamdan En Büyük Terimi Bulma (Çift Terim Sayısı)

**Soru:** Ardışık 6 tek sayının toplamı `96` ise, bu sayıların en büyüğü
kaçtır?

**Çözüm:**
- Terim sayısı `6` (çift) → gerçek bir ortadaki sayı yoktur, "aradaki
  sayı" kullanılır.
- Aradaki sayı: `96 / 6 = 16`.
- `16`, ardışık tek sayı dizisinde iki terimin (`15` ve `17`) tam
  ortasındadır.
- En büyüğe ulaşmak için `17`'den sağa doğru `2` terim daha ilerlenir
  (`6` terimin `3`'ü sağda): `17, 19, 21`.
- **Sonuç: En büyük sayı `21`'dir.**

<a id="ornek-7"></a>
## Örnek 7 — N. Terimi Bulma (Baştan Sayarak)

**Soru:** Ardışık 15 çift sayının toplamı `330`'dur. Sayılar küçükten
büyüğe sıralandığında, baştan 9. sayı kaçtır?

**Çözüm:**
- Terim sayısı `15` (tek) → ortadaki sayı gerçek bir üyedir ve tam
  olarak `8`. sayıdır (`7` terim solda, `7` terim sağda).
- Ortadaki sayı: `330 / 15 = 22`.
- `22`, `8`. terimdir. `9`. terim ondan bir adım (çift sayıda `2`)
  sonrasıdır: `22 + 2 = 24`.
- **Sonuç: Baştan 9. sayı `24`'tür.**

<a id="ornek-8"></a>
## Örnek 8 — İki Ayrı Ardışık Grubun Ortak Toplamı

**Soru:** Ardışık 3 pozitif tek sayı ile ardışık 3 pozitif çift sayının
toplamı `117`'dir. Bu tek sayıların en büyüğü en fazla kaç olabilir?

**Çözüm:**
- Tek sayıların en büyüğünün maksimum olması için, çift sayıların
  toplamının **minimum** olması gerekir (117 sabit olduğundan, biri
  küçüldükçe diğerine daha fazla pay kalır).
- En küçük 3 pozitif ardışık çift sayı: `2, 4, 6` → toplamları `12`.
- Kalan tek sayıların toplamı: `117 - 12 = 105`.
- Bu `105`, ardışık 3 tek sayının toplamı olduğundan ortadaki sayı:
  `105 / 3 = 35`.
- Ortadaki `35` olduğuna göre dizinin en büyüğü: `35 + 2 = 37`.
- **Sonuç: Tek sayıların en büyüğü en fazla `37` olabilir.**

<a id="ornek-9"></a>
## Örnek 9 — Kalan Toplamdan Çıkarılan Terimleri Bulma

**Soru:** `1`'den `39`'a kadar numaralı `39` top bir torbadadır.
İçlerinden numaraları ardışık tek sayı olan `5` top çıkarılıyor. Kalan
topların numaraları toplamı `645`'tir. Çıkarılan toplardan en küçük
numaralı olanının numarası kaçtır?

**Çözüm:**
- `1`'den `39`'a kadar tüm topların toplamı:
  `39 × 40 / 2 = 780`.
- Çıkarılan 5 topun toplamı: `780 - 645 = 135`.
- Bu 5 top ardışık tek sayı olduğundan ortadaki sayı: `135 / 5 = 27`.
- `27` ortadaysa, dizinin en küçüğü iki adım (`2 + 2`) öncesindedir:
  `27 - 2 - 2 = 23`.
- **Sonuç: Çıkarılan en küçük numaralı top `23` numaralıdır.**

<a id="ornek-10"></a>
## Örnek 10 — Artı Yerine Eksi Konan Terimi Bulma

**Soru:** `1`'den `15`'e kadar numaralı toplar üzerindeki numaralar
toplanmak isteniyor, fakat toplarken bir topun numarasının önüne
yanlışlıkla `+` yerine `-` konuyor ve sonuç `96` bulunuyor. Yanlışlıkla
önüne eksi konan topun numarası kaçtır?

**Çözüm:**
- Doğru toplam (hata olmasaydı): `15 × 16 / 2 = 120`.
- Bulunan (yanlış) toplam: `96`.
- Fark: `120 - 96 = 24`.
- Bir terimin önüne eksi konması, o terimi hem toplamamak hem de bir
  kez fazladan çıkarmak anlamına geldiğinden, toplamdaki azalma o
  terimin **2 katı** kadardır: `24 = 2 × terim`.
- **Sonuç: Eksi konan topun numarası `24 / 2 = 12`'dir.**

<a id="ornek-11"></a>
## Örnek 11 — En Az / En Çok Aralığında Alınabilecek Değer Sayısı

**Soru:** `1`'den `10`'a kadar numaralı kutuların her birine, kutunun
üzerindeki sayı kadar kalem konulmak isteniyor. Ancak kutulardan
**üçüne**, üzerlerindeki sayı kadar **iki kez** (yani bir fazladan)
kalem konuyor. Buna göre tüm kutulardaki toplam kalem sayısı kaç farklı
değer alabilir?

**Çözüm:**
- Standart durumda (hatasız) toplam kalem sayısı:
  `10 × 11 / 2 = 55`.
- Fazladan konan kalemler, seçilen `3` kutunun üzerindeki sayıların
  toplamı kadar **ilave** kalem demektir.
- **En az ilave** için en küçük `3` kutu seçilir: `1+2+3=6` →
  toplam kalem: `55 + 6 = 61`.
- **En çok ilave** için en büyük `3` kutu seçilir: `8+9+10=27` →
  toplam kalem: `55 + 27 = 82`.
- `61` ile `82` arasındaki her tam sayı değeri, farklı üçlü kutu
  seçimleriyle elde edilebilir (aradaki tüm değerler alınabilir).
- Alınabilecek farklı değer sayısı: `82 - 61 + 1 = 22`.
- **Sonuç: Toplam kalem sayısı `22` farklı değer alabilir.**

<a id="ornek-12"></a>
## Örnek 12 — Toplamın 5'in Katı Olması Koşulundan `n` Değerlerini Bulma

**Soru:** `n` pozitif tam sayı ve `n ≤ 24` olmak üzere, `1`'den `n`'e
kadar olan sayıların toplamı `5`'in tam katı bir sayıya eşittir. Buna
göre `n` kaç farklı değer alabilir?

**Çözüm:**
- Toplam formülü: `n × (n + 1) / 2`. Bu ifadenin `5`'in katı olması
  için, `n` ile `n + 1` çarpanlarından **birinin `5`'in katı** olması
  yeterlidir (2'ye bölme paritesini etkilemez).
- `n`'in kendisi `5`'in katıysa: `n = 5, 10, 15, 20` (4 değer, `24`
  sınırı içinde).
- `n + 1` ifadesi `5`'in katıysa, yani `n` bir eksiği `5`'in katından:
  `n = 4, 9, 14, 19` (4 değer, `24` sınırı içinde; `n = 24` bir sonraki
  aday olurdu ama `25`'in bir eksiği olan `24` de aslında bu gruba
  girer — sınır kontrolüyle uygun olanlar sayılır).
- Bu iki grup toplamda `n`'e **8 farklı değer** kazandırır.
- **Sonuç: `n`, `8` farklı değer alabilir.**

<a id="ornek-13"></a>
## Örnek 13 — Her Terim Sabit Miktar Artırılırsa Toplamdaki Artış

**Soru:** `2, 5, 8, ..., 62` şeklinde giden ardışık toplamdaki her bir
terim `5` artırılırsa, toplam kaç artar?

**Çözüm:**
- Önce terim sayısı bulunur: artış miktarı `3` olduğundan
  `(62 - 2) / 3 + 1 = 20 + 1 = 21` terim vardır.
- Her terim `5` arttığında toplamdaki artış, terim sayısı ile terim
  başına artışın çarpımıdır: `21 × 5 = 105`.
- **Sonuç: Toplam `105` artar.**

<a id="ornek-14"></a>
## Örnek 14 — Çarpımsal Terimlerde Tek Çarpan Artışının Etkisi

**Soru:** `1×2 + 2×3 + 3×4 + ... + 15×16` toplamındaki her terimin
**ikinci çarpanı** `5` artırılırsa (yani terimler `1×7, 2×8, 3×9, ...,
15×20` olursa), toplam kaç artar?

**Çözüm:**
- Her terimde **değişmeyen** ilk çarpanlar (`1, 2, 3, ..., 15`) zihinsel
  olarak silinir; geriye bu çarpanların oluşturduğu **yeni bir ardışık
  toplam** kalır: `1 + 2 + 3 + ... + 15`.
- Bu toplam: `15 × 16 / 2 = 120`.
- Bulunan bu toplam, terimin arttığı miktarla (`5`) çarpılır:
  `120 × 5 = 600`.
- **Sonuç: Toplam `600` artar.** (Her terimi tek tek yeniden çarpıp eski
  toplamdan çıkarmaktan çok daha hızlı bir yoldur.)

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

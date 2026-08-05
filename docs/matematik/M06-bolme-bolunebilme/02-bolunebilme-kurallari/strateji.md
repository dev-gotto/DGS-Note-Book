# 🎯 Soru Çözüm Stratejileri — bölünebilme kuralları

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Kuralı Olan Sayılarda Sabit Refleks: Önce Basamak, Sonra Rakam Toplama

Bir sayı birden fazla bölünebilme koşulunu aynı anda sağlıyorsa (ör. hem
3'e hem 5'e), koşullar rastgele sırayla değil, **basamak bakarak
kontrol edilen kurallar** (2, 4, 5, 8, 10) **önce**, **rakamları
toplayarak kontrol edilen kurallar** (3, 9, 11) **en son** uygulanır.
Basamak kuralları bilinmeyeni doğrudan sınırlı bir kümeye (genelde tek
bir değere) indirger; rakam toplama kuralları bu daralmış küme üzerinde
çok daha hızlı elenir.

## Kuralı Olmayan Sayıyı Aralarında Asal İki Çarpana Ayırma

15, 30, 36, 45, 88, 99 gibi kendine ait kuralı olmayan bir sayıyla
karşılaşınca ilk iş, sayıyı **aralarında asal** (ortak böleni 1'den
başka olmayan) ve **her ikisinin de kendine ait bölünebilme kuralı
olan** iki çarpana ayırmaktır (bkz. pratik.md — Sık Kullanılan
Ayrımlar tablosu). Sayı bu iki çarpana ayrı ayrı tam bölünüyorsa,
orijinal sayıya da tam bölünür.

## "Bir Şey Olmuşsa Olmuştur" — Tek Cevap Arayan Sorularda Erken Durma

Soru "kaçtır" gibi tek bir kesin değer istiyorsa (en az/en çok değil),
koşulları sağlayan ilk uygun deneme bulunduğu an iş bitmiştir; kalan
ihtimalleri de tek tek doğrulamaya gerek yoktur (bkz. Örnek 7).

## "Biri Yanlış" Türü Mantık Sorularında Sistematik Eleme

Birden fazla bölünebilme bilgisi verilip bunlardan yalnızca birinin
yanlış olduğu söylenirse, rastgele deneme yapılmaz. Bilgiler arasında
**mantıksal içerme ilişkisi** aranır: eğer bir bilgi doğruyken başka
bir bilgiyi zorunlu olarak doğru kılıyorsa (ör. 10'a bölünmek 2'ye ve
5'e bölünmeyi de zorunlu kılar), o bilgi yanlış olamaz — çünkü yanlış
olsaydı en az iki bilgi daha çökerdi. Yanlış olan bilgi, böyle bir
içerme zincirinin **en güçlü ucunda** (ör. 9'a bölünme, 3'e bölünmeyi
zorunlu kılan taraf) aranmalıdır (bkz. Örnek 6).

---

<a id="ornek-1"></a>
## Örnek 1 — Palindrom Sayıda Çoklu Bölünebilme Koşulunu Birleştirme

**Soru:** $a, b$ birer rakam olmak üzere, dört basamaklı
$\overline{abba}$ doğal sayısı hem $5$ hem de $3$ ile tam
bölünmektedir. Ayrıca $b$ rakamının kendisiyle oluşturduğu iki
basamaklı $\overline{bb}$ sayısı $4$ ile tam bölünmektedir. Buna göre
$a+b$ toplamı kaçtır?

**Çözüm:**
- Önce **basamak bazlı** kurallara bakılır (2, 4, 5, 8, 10 sıralaması),
  rakam toplama kuralı (3) en sona bırakılır.
- $\overline{bb}$ sayısı $4$'e bölünüyor: aynı rakamdan oluşan iki
  basamaklı sayılar arasında yalnızca $00, 44, 88$ dörde tam bölünür
  (tekler zaten elenir: $11, 33, 55, 77, 99$; çiftlerden $22, 66$
  bölünmez). Demek ki $b \in \{0,4,8\}$.
- $\overline{abba}$ sayısı $5$'e bölünüyor: sondaki rakam $a$ olduğu
  için $a=0$ ya da $a=5$; $a$ başta olduğundan $0$ olamaz →
  $a=5$.
- Sayı artık $\overline{5bb5}$. $3$'e bölünmesi için rakamları toplamı
  ($5+b+b+5 = 10+2b$) $3$'ün katı olmalı.
  - $b=0$: toplam $10$ → olmaz.
  - $b=4$: toplam $18$ → **olur.**
  - $b=8$: toplam $26$ → olmaz.
- Demek ki $b=4$, sayı $5445$.
- **Sonuç: $a+b = 5+4 = 9$ (C seçeneği).**

<a id="ornek-2"></a>
## Örnek 2 — Faktöriyel + 8 ile Bölünebilme: Sondan Basamak Mantığı

**Soru:** $53! - 22$ sayısının $8$ ile bölümünden kalan kaçtır?

**Çözüm:**
- $8 = 2^3$ olduğu için bu sayının $8$'e bölümünden kalanını bulmak
  için yalnızca **son 3 basamağa** bakmak yeterlidir.
- $53!$ sayısının sondan sıfır sayısı (asal çarpanlara ayırmadaki $5$
  kuvveti: $\lfloor 53/5 \rfloor + \lfloor 53/25 \rfloor = 10+2=12$)
  $3$'ten çok daha fazla olduğu için $53!$'in son 3 basamağı
  **000**'dır.
- $53! - 22$ işleminde son 3 basamak $1000 - 22 = 978$'e döner (komşu
  basamaktan ödünç alınır).
- $978$'i $8$'e böl: $8 \times 122 = 976$, kalan $2$.
- **Sonuç: kalan $2$.**

<a id="ornek-3"></a>
## Örnek 3 — ÖSYM Tarzı: Üç Bağlantılı İki Basamaklı Sayıyla Rakam Bulma

**Soru:** $a, b, c$ birbirinden farklı rakamlar olmak üzere; iki
basamaklı $\overline{ab}$ sayısı $5$'e, iki basamaklı $\overline{bc}$
sayısı $9$'a, iki basamaklı $\overline{ca}$ sayısı $4$'e tam
bölünmektedir. Buna göre $a+b+c$ toplamı kaçtır?

**Çözüm:**
- $\overline{ab}$, $5$'e bölünüyor → $b=0$ ya da $b=5$; $b$ bir iki
  basamaklı sayının ($\overline{bc}$) baş rakamı olduğu için $0$
  olamaz → $b=5$.
- $\overline{bc}$, $9$'a bölünüyor → $b+c$ toplamı $9$'un katı olmalı:
  $5+c=9$ → $c=4$.
- $\overline{ca}$, $4$'e bölünüyor → $\overline{4a}$ dörde tam
  bölünmeli: $a \in \{0,4,8\}$; $a$ başta olduğu için $0$ olamaz,
  $c=4$ olduğu için (rakamlar farklı) $4$ de olamaz → $a=8$.
- **Kontrol:** $\overline{ab}=85$ ($85\div5=17$ ✓), $\overline{bc}=54$
  ($54\div9=6$ ✓), $\overline{ca}=48$ ($48\div4=12$ ✓).
- **Sonuç: $a+b+c = 8+5+4 = 17$ (D seçeneği).**

<a id="ornek-4"></a>
## Örnek 4 — 10 Kuralıyla Son Rakamı Sabitleyip 3 Kuralıyla Aralığı Bulma

**Soru:** Beş basamaklı $\overline{54A2B}$ sayısının $10$ ile
bölümünden kalan $5$'tir. Bu sayı aynı zamanda $3$ ile tam
bölünmektedir. Buna göre $A$'nın alabileceği değerlerin toplamı
kaçtır?

**Çözüm:**
- $10$'a bölümünden kalan $5$ ise, kalan doğrudan **birler
  basamağıdır** (10 kuralında tek ihtimal vardır) → $B=5$.
- Sayı artık $\overline{54A25}$. $3$'e bölünmesi için rakamları
  toplamı ($5+4+A+2+5 = 16+A$) $3$'ün katı olmalı.
- $16+A$'yı $3$'e tamamlayan en küçük $A$: $A=2$ ($18$). Sonra üçer
  üçer artarak: $A=5$ ($21$), $A=8$ ($24$).
- $A \in \{2,5,8\}$.
- **Sonuç: toplam $2+5+8=15$ (A seçeneği).**

<a id="ornek-5"></a>
## Örnek 5 — İç İçe Kalan İşlemi: Önce 11, Sonra 10 Kuralı

**Soru:** Pozitif tam sayılarda tanımlanan $A \boxed{B}$ işlemi,
$A$'nın $B$'ye bölümünden kalanı verir. Bir sayı $19523 \boxed{\left(
\overline{3A81A} \boxed{11} \right)}$ biçiminde tanımlanıyor. Buna göre
bu işlemin sonucu kaçtır?

**Çözüm:**
- Önce iç işlem çözülür: $\overline{3A81A}$'nın $11$'e bölümünden
  kalanı bul.
- $11$ kuralı: sağdan başlayarak $+,-,+,-,+$ işareti ver: en sağdaki
  $A$ ($+$), $1$ ($-$), $8$ ($+$), soldan ikinci $A$ ($-$), en soldaki
  $3$ ($+$).
- $A$'lar birbirini götürür ($+A-A=0$); geriye $-1+8+3=10$ kalır.
- $10$, $0$–$11$ aralığında olduğu için doğrudan kalandır: iç işlemin
  sonucu $10$.
- Şimdi dış işlem: $19523 \boxed{10}$, yani $19523$'ün $10$'a bölümünden
  kalanı. $10$ kuralında kalan doğrudan **birler basamağıdır**: sonu
  $3$ olduğu için kalan $3$.
- **Sonuç: $3$.**

<a id="ornek-6"></a>
## Örnek 6 — "Biri Yanlış" Mantık Sorusu: İçerme İlişkisiyle Yanlışı Bulma

**Soru:** $A$ doğal sayısı için "$2$ ile tam bölünür", "$3$ ile tam
bölünür", "$5$ ile tam bölünür", "$9$ ile tam bölünür", "$10$ ile tam
bölünür" bilgilerinden $4$'ü doğru, yalnızca $1$'i yanlıştır. Buna göre
$A$ sayısı aşağıdakilerden hangisine tam bölünemez?
A) 45  B) 6  C) 10  D) 15  E) 30

**Çözüm:**
- "$10$'a bölünür" yanlış olsaydı, $10=2\times5$ olduğundan "$2$'ye" ve
  "$5$'e bölünür" bilgileri de otomatik yanlış olurdu — bu, en az $3$
  bilginin yanlış olması demektir, koşulla ($1$ yanlış) çelişir. Demek
  ki "$10$'a", "$2$'ye", "$5$'e bölünür" bilgilerinin **üçü de doğru**.
- "$9$'a bölünür" doğru olsaydı, $9$'un katı olan her sayı $3$'ün de
  katı olduğundan "$3$'e bölünür" de zorunlu doğru olurdu — bu durumda
  $5$ bilginin hepsi doğru olur, "$1$ yanlış" koşuluyla çelişir.
  Demek ki yanlış olan bilgi **"$9$'a bölünür"**dür; "$3$'e bölünür"
  doğrudur.
- Sonuç: $A$; $2$'ye, $3$'e, $5$'e, $10$'a bölünür ama **$9$'a
  bölünmez**.
- Seçenekleri kontrol et: $45 = 9\times5$ — $A$, $9$'a bölünmediği için
  $45$'e de tam bölünemez. Diğerleri ($6=2\times3$, $10$, $15=3\times5$,
  $30=2\times3\times5$) $A$'nın kesin bölündüğü sayıların çarpımlarından
  oluşuyor, dolayısıyla hepsine bölünür.
- **Sonuç: A sayısı $45$'e tam bölünemez (A seçeneği).**

<a id="ornek-7"></a>
## Örnek 7 — Dört Kombinasyonlu Rakam Sorusunda İlk Uygun Denemeyi Kabul Etme

**Soru:** $0$'dan farklı $a$ ve $b$ rakamlarıyla oluşturulan tüm iki
basamaklı sayılar ($\overline{ab}$, $\overline{ba}$, $\overline{aa}$,
$\overline{bb}$) $2$'ye tam bölünmektedir. Bu dört sayının yarısı
$3$'e tam bölünmekte, yarısı bölünmemektedir. Bu dört sayıdan yalnızca
biri $8$'e tam bölünmektedir. Buna göre $a \times b$ çarpımı kaçtır?

**Çözüm:**
- Dört sayının hepsi $2$'ye bölünüyorsa, $a$ ve $b$ ikisi de **çift**
  rakam olmalı ($0$ hariç): aday kümesi $\{2,4,6,8\}$.
- $a=2, b=4$ dene: sayılar $24, 42, 22, 44$.
  - $3$'e bölünenler: $24$ ($2+4=6$ ✓), $42$ ($4+2=6$ ✓); $22$ ve $44$
    bölünmüyor → tam **yarısı** ($2/4$) sağlanıyor ✓.
  - $8$'e bölünen: yalnızca $24$ ($24\div8=3$); $42, 22, 44$ bölünmüyor
    → **sadece bir tanesi** koşulu sağlanıyor ✓.
- Bu deneme tüm koşulları ilk seferde sağladığı için ("bir şey olmuşsa
  olmuştur" ilkesi) başka kombinasyon aranmasına gerek yoktur.
- **Sonuç: $a \times b = 2 \times 4 = 8$ (A seçeneği).**

<a id="ornek-8"></a>
## Örnek 8 — "Geometrik Sayı" Uydurma Tanımını Mevcut Kurallara İndirgeme

**Soru:** İçine yazıldığı çokgenin kenar sayısına tam bölünen sayılara
"geometrik sayı" denir. İki basamaklı $\overline{ab}$ sayısı bir
üçgenin içine, iki basamaklı $\overline{ba}$ sayısı bir beşgenin
içine yazılmış ve ikisi de geometrik sayıdır. Buna göre
$\overline{ab}$ sayısının alabileceği değerlerin toplamı kaçtır?

**Çözüm:**
- Tanım okunup mevcut kurallara indirgenir: üçgen → $3$'e bölünmeli,
  beşgen → $5$'e bölünmeli.
- $\overline{ba}$, $5$'e bölünüyor → sondaki rakam $a$; $a=0$ ya da
  $a=5$. $\overline{ab}$'de $a$ baştaki rakam olduğu için $0$ olamaz →
  $a=5$.
- $\overline{ab} = \overline{5b}$, $3$'e bölünüyor → $5+b$ toplamı
  $3$'ün katı olmalı. En küçük uygun $b$: $1$ ($5+1=6$), sonra üçer
  üçer: $4$ ($9$), $7$ ($12$).
- $\overline{ab}$'nin alabileceği değerler: $51, 54, 57$.
- **Sonuç: $51+54+57 = 162$ (D seçeneği).**

<a id="ornek-9"></a>
## Örnek 9 — Kuralı Olmayan Sayıda "En Büyük Değer" Sorusu

**Soru:** Beş basamaklı $\overline{6A32B}$ sayısı $15$'e tam
bölünmektedir. Buna göre $A+B$ toplamının en büyük değeri kaçtır?

**Çözüm:**
- $15 = 3 \times 5$; sıra kuralı gereği önce **5**'e, sonra **3**'e
  bakılır.
- $5$'e bölünmesi için sondaki $B$ rakamı $0$ ya da $5$; $A+B$ en
  büyük isteniyorsa $B=5$ seçilir.
- Sayı artık $\overline{6A325}$. $3$'e bölünmesi için rakamları
  toplamı ($6+A+3+2+5 = 16+A$) $3$'ün katı olmalı: $A \in \{2,5,8\}$
  (üçer üçer artarak).
- $A+B$'yi en büyük yapmak için $A$'nın en büyük değeri seçilir:
  $A=8$.
- **Sonuç: $A+B = 8+5 = 13$ (C seçeneği).**

<a id="ornek-10"></a>
## Örnek 10 — Rakamları Farklı Kısıtıyla Çok Dallı Bir 36 Sorusu

**Soru:** Beş basamaklı, rakamları birbirinden farklı $\overline{8AB7C}$
doğal sayısı $36$'ya tam bölünmektedir. Buna göre $A+B+C$ toplamının
en büyük değeri kaçtır?

**Çözüm:**
- $36 = 4 \times 9$; önce **4**'e, sonra **9**'a bakılır.
- $4$'e bölünmesi için son iki rakam ($\overline{7C}$) dörde tam
  bölünmeli: kontrol edilince yalnızca $C=2$ ($72$) ve $C=6$ ($76$)
  uyuyor.
- **$C=2$ dalı:** sayı $\overline{8AB72}$. $9$'a bölünmesi için
  rakamlar toplamı ($8+A+B+7+2=17+A+B$) $9$'un katı olmalı:
  $A+B \in \{1, 10\}$ (rakamlar $0$–$9$ arası olduğundan üst sınır
  aşılmaz). En büyük toplam için $A+B=10$ seçilir → bu dalda
  $A+B+C = 10+2 = 12$.
- **$C=6$ dalı:** sayı $\overline{8AB76}$. Rakamlar toplamı
  ($21+A+B$) $9$'un katı olmalı: $A+B \in \{6, 15\}$.
  - $A+B=15$ denendiğinde, rakamlar farklı olma şartı yüzünden
    ($8, 7, 6$ zaten kullanılmış) uygun bir $(A,B)$ çifti bulunamıyor
    (kalan rakamların en büyük ikilisi bile $9+5=14$'te kalıyor) →
    **elenir**.
  - Demek ki bu dalda $A+B=6$ geçerli → $A+B+C = 6+6 = 12$.
- İki dal da aynı en büyük değeri veriyor.
- **Sonuç: $A+B+C$ en büyük değeri $12$ (B seçeneği).**

<a id="ornek-11"></a>
## Örnek 11 — Kalanlı Kuralsız Sayı Sorusu: Kalanı Her İki Çarpana da Uygulama

**Soru:** Beş basamaklı $\overline{6A32B}$ sayısının $30$ ile
bölümünden kalan $1$'dir. Buna göre $A$'nın alabileceği değerlerin
toplamı kaçtır?

**Çözüm:**
- $30$'un kuralı yok; $30 = 3 \times 10$ (aralarında asal) olarak
  ayrılır. **$30$'a bölümünden kalan $1$ ise, aynı kalan hem $10$'a
  hem $3$'e bölümünde de geçerlidir.**
- $10$'a bölümünden kalan $1$ → sondaki rakam $B=1$.
- Sayı artık $\overline{6A321}$. $3$'e bölümünden kalan $1$ olmalı:
  rakamlar toplamı ($6+A+3+2+1 = 12+A$); $12$ zaten $3$'ün katı
  olduğundan kalan doğrudan $A$'nın $3$'e bölümünden kalanına eşittir
  → $A$'nın $3$'e bölümünden kalanı $1$ olmalı: $A \in \{1,4,7\}$.
- **Sonuç: toplam $1+4+7 = 12$ (C seçeneği).**

<a id="ornek-12"></a>
## Örnek 12 — Çok Koşullu Şifre Sorusu: 5, 4, 3 Kurallarını Zincirleme

**Soru:** Rakamları birbirinden farklı, altı basamaklı
$\overline{5A36BC}$ doğal sayısı $12$'ye tam bölünmektedir. Bu sayının
$5$'e bölümünden kalan $2$'dir. Buna göre $A$'nın alabileceği farklı
değerlerin toplamı kaçtır?

**Çözüm:**
- $5$'e bölümünden kalan $2$ ise, sondaki $C$ rakamı $2$ ya da $7$
  olabilir.
- $12 = 4 \times 3$; önce $4$'e bakılır: son iki rakam
  ($\overline{BC}$) dörde bölünmeli, bu da $C$'nin **çift** olmasını
  gerektirir → $C=7$ (tek) elenir, $C=2$ kalır.
- $\overline{B2}$'nin $4$'e bölünmesi için $B$ **tek** olmalı:
  $B \in \{1,3,5,7,9\}$; rakamlar farklı olduğundan sayıda zaten
  kullanılan $3$ ve $5$ elenir → $B \in \{1,7,9\}$.
- Her $B$ için $9$'a değil $3$'e bakılır (rakamlar toplamı
  $5+3+6+2+A+B = 16+A+B$ üçün katı olmalı), ve rakamların farklılığı
  ayrıca kontrol edilir:
  - $B=1$: $17+A$ üçün katı → $A \in \{1,4,7\}$; $A=1$ ise $B$ ile
    çakışır, elenir → $A \in \{4,7\}$.
  - $B=7$: $23+A$ üçün katı → adaylar arasından $B$ ile çakışan ($7$)
    elenir; kalanlar önceki dalla aynı kümeye düşer, yeni bir değer
    eklemez.
  - $B=9$: $25+A$ üçün katı → $A \in \{2,5,8\}$; $2$ ve $5$ sayıda
    zaten var, elenir → yalnızca $A=8$ kalır.
- Tüm dallardan gelen farklı $A$ değerleri: $\{4, 7, 8\}$.
- **Sonuç: toplam $4+7+8 = 19$ (D seçeneği).**

<a id="ornek-13"></a>
## Örnek 13 — Asal Sayı Kısıtıyla 11 ve 3 Kuralını Birlikte Kullanma

**Soru:** $A$ bir asal sayı olmak üzere, beş basamaklı $\overline{3A5B1}$
doğal sayısı $33$'e tam bölünmektedir. Bu koşulu sağlayan kaç farklı
$\overline{3A5B1}$ sayısı yazılabilir?

**Çözüm:**
- $33 = 3 \times 11$; önce $11$'e bakılır.
- $11$ kuralı: sağdan başlayarak $+,-,+,-,+$: $1(+) \; B(-) \; 5(+) \;
  A(-) \; 3(+)$ → toplam $= 1-B+5-A+3 = 9-A-B$.
- Bu değer $0$ ya da (rakam toplamlarının sınırları içinde) $\pm11$
  olmalı; $A,B$ birer rakam olduğundan $A+B$ en çok $18$ olabilir, bu
  yüzden yalnızca $9-A-B=0$ mantıklı, yani $A+B=9$.
- $3$'e bölünme kontrolü: rakamlar toplamı $A+3+5+B+1 = 9+A+B$;
  $A+B=9$ olduğunda bu toplam $18$ olur, ki bu zaten $3$'ün katıdır —
  demek ki $A+B=9$ koşulu $3$'e bölünmeyi otomatik olarak sağlıyor.
- $A$ asal bir rakam olduğuna göre $A \in \{2,3,5,7\}$; $A+B=9$
  koşulundan $B$'yi bul: $(A,B) \in \{(2,7),(3,6),(5,4),(7,2)\}$ —
  $4$ farklı çift.
- **Sonuç: $4$ farklı sayı yazılabilir (C seçeneği).**

<a id="ornek-14"></a>
## Örnek 14 — 11'e Bölmenin Bölüm Kısayolunu Gerçek Bir Soruda Kullanma

**Soru:** Üç basamaklı $\overline{4A3}$ ve $\overline{6BC}$ doğal
sayılarının $11$ ile bölümünden elde edilen bölümlerin toplamı $100$'dür.
Buna göre $A+B+C$ toplamı kaçtır?

**Çözüm:**
- **$\overline{4A3}$ için:** baştaki ile sondaki rakamın toplamı
  ($4+3=7$) doğrudan ortadaki rakamı veriyor → $A=7$, sayı $473$'tür.
  Bölüm kısayolu: ortadaki rakam silinir → bölüm $=43$.
- **$\overline{6BC}$ için:** iki bölümün toplamı $100$ olduğuna göre bu
  sayının bölümü $100-43=57$'dir.
- $57$'nin **bölüm kısayolundan geri gitme**: bölüm iki basamaklıysa
  ve baştaki rakam ($6$'dan) bir azaltılmış görünüyorsa ($6 \to 5$),
  bu "eksili" (11 çıkarmalı) durumdur → $\overline{6BC}$'de baştaki
  ile sondaki toplamdan ortadakini çıkarınca $11$ elde ediliyor demektir
  ve bölümün son rakamı doğrudan $C$'ye eşittir → $C=7$.
- Eksili durumun denklemi: $6+C-B=11$ → $6+7-B=11$ → $B=2$.
- **Kontrol:** $627 \div 11 = 57$ ✓ ($57 \times 11 = 627$).
- **Sonuç: $A+B+C = 7+2+7 = 16$ (D seçeneği).**

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

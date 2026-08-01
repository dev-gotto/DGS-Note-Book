# 🎯 Soru Çözüm Stratejileri — basamak kavramı

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Çözümleme mi Benzetme mi Kullanılacağını Seçme Stratejisi

İfadedeki harf/basamak sayısı azsa (2-3 basamaklı tek bir sayı gibi)
doğrudan çözümleme yap. İfadede aynı bloğun (örn. iki basamaklı bir sayı)
birden fazla yerde tekrar ettiğini görürsen, çözümlemek yerine o bloğu
`x` ile göster (benzetme); işlemi tek adımda bitirir.

## Rakamları Farklı mı Aynı mı Olabilir Kontrolü

Soruya başlamadan önce metinde "rakamlar birbirinden farklıdır" ibaresi
olup olmadığını kontrol et. Yoksa, en büyük/en küçük değer ararken aynı
rakamı iki harfe birden vermekten çekinme.

## Denklemi Sadeleştirip Değer Verme Stratejisi

Harfli bir denklem kurduktan sonra tek bir bilinmeyene indirgemek her
zaman mümkün olmayabilir; böyle durumlarda denklemi `A × sabit = B ×
sabit` gibi bir orana getirip, `A` ve `B`'ye rakam sınırları (`0-9`)
içinde uygun değerler vererek ilerle — en büyük/en küçük isteniyorsa
sınır değerlerden (`9` veya `1`) başla.

## Basamak Artış/Azalışını Somut Bir Sayı Üzerinde Doğrulama Stratejisi

Basamak artış/azalış sorularında cebirsel çözümün yanında, şartlara
uygun rastgele bir sayı seçip değişikliği o sayı üzerinde uygulamak da
aynı sonucu verir ve hata riskini azaltır; iki yöntemle çapraz kontrol
yapılabilir.

## Sütun Toplama/Çıkarma Bulmacalarında Sondan Başlama Stratejisi

Harfli sütun toplama/çıkarma (alt alta yazılmış) sorularında **birler
basamağından** başla; her sütunda elde var mı yok mu (toplamada) veya
komşudan onluk almak gerekiyor mu (çıkarmada) kontrol ederek bir üst
sütuna geç. Harfleri bu zincirleme mantıkla teker teker bul.

## Mantık Sorularında "Kaç Farklı Sayı Yazılabilir" Sayma Stratejisi

Bir grup arkadaşın/kişinin verdiği bilgiyle "tahmin edemediler" tipi
mantık sorularında, aranan koşulu sağlayan sayıların **toplam adedi**,
tahmin eden kişi sayısından **fazla** olmalıdır (aksi hâlde biri kesin
tahmin ederdi). Koşulu sağlayan sayıları sistematik olarak listeleyip
sayarak ilerle.

---

<a id="ornek-1"></a>
## Örnek 1 — Çevrimsel Toplam ile Kısa Yoldan Değer Bulma

**Soru:** `x`, `y`, `xyx` ve `yxy` üç basamaklı doğal sayılardır.
`x + y = 3` olduğuna göre `xyx + yxy` nedir?

**Çözüm:**
- `xyx = 100x + 10y + x = 101x + 10y`
- `yxy = 100y + 10x + y = 101y + 10x`
- Toplarsan: `111x + 111y = 111(x+y)`
- `x + y = 3` verilmiş → `111 × 3 = 333`
- **Sonuç: `333`.**

<a id="ornek-2"></a>
## Örnek 2 — Fark Denkleminden Rakamları Bulup Toplama

**Soru:** `AB` ve `BA` iki basamaklı doğal sayılardır. `AB - BA = 63`
olduğuna göre bu koşulu sağlayan `AB` sayılarının toplamı kaçtır?

**Çözüm:**
- `AB - BA = 9(A - B) = 63` → `A - B = 7`.
- Hem `AB` hem `BA` iki basamaklı sayı olduğu için `A ≠ 0` **ve**
  `B ≠ 0` olmalı (yani `B = 0, A = 7` seçeneği geçersiz, çünkü `BA`
  o zaman `07` olurdu).
- `A - B = 7` ve `B ≠ 0` şartını sağlayan rakam çiftleri: `A=8, B=1`
  (`AB=81`) ve `A=9, B=2` (`AB=92`). Kontrol: `81-18=63` ✓, `92-29=63` ✓.
- Bu koşulu sağlayan tüm `AB` sayılarının toplamı: `81 + 92 = 173`.
- **Sonuç: `173` (D seçeneği).**

<a id="ornek-3"></a>
## Örnek 3 — En Büyük Değer İçin Sınır Rakamları Kullanma

**Soru:** `ABC` ve `CBA` 3 basamaklı doğal sayılardır. `ABC - CBA = 792`
olduğuna göre `ABC` sayısının en büyük değeri kaçtır?

**Çözüm:**
- `ABC - CBA = 99(A - C) = 792` → `A - C = 8`
- `A - C = 8`'i sağlayan en büyük `A` değeri `9`, buna karşılık `C = 1`.
- Soru rakamların farklı olmasını istemediği için `B`'ye verilebilecek
  en büyük değer `9`'dur.
- `A=9, B=9, C=1` → `ABC = 991`.
- **Sonuç: `991` (D seçeneği).**

<a id="ornek-4"></a>
## Örnek 4 — Katlı İfadeyi Denkleme Çevirip Bölme

**Soru:** 3 basamaklı `5MM` sayısı ile 2 basamaklı `7M` sayısının
toplamı, `M` rakamının `107` katına eşittir. `M` kaçtır?

**Çözüm:**
- `5MM = 500 + 10M + M = 500 + 11M`
- `7M = 70 + M`
- Toplam: `500 + 11M + 70 + M = 570 + 12M`
- Denklem: `570 + 12M = 107M` → `570 = 95M` → `M = 6`.
- **Sonuç: `M = 6` (D seçeneği).**

<a id="ornek-5"></a>
## Örnek 5 — Baştan Benzetme ile İfade Yazma

**Soru:** İki basamaklı `AB` sayısı `x` ile gösterilirse, `2AB` (üç
basamaklı) sayısının değeri `x` cinsinden nedir?

**Çözüm:**
- `2AB` sayısındaki baştaki `2`'yi çıkarırsan geriye `AB` kalır.
- `2`'nin basamak değeri `200`'dür.
- `2AB = 200 + AB = 200 + x`.
- **Sonuç: `200 + x`.**

<a id="ornek-6"></a>
## Örnek 6 — Sondan Benzetme ile İfade Yazma

**Soru:** İki basamaklı `AB` sayısı `x` ile gösterilirse, `3AB2` (dört
basamaklı) sayısının değeri `x` cinsinden nedir?

**Çözüm:**
- `AB`'yi ortadan çıkarırsan geriye `3002` kalır (`AB`'nin yerine `00`
  gelir).
- Ama `AB`'nin basamak değerini de eklemek gerekir: `AB` onlar ve
  yüzler basamağında olduğu için değeri `10 × AB = 10x`'tir.
- `3AB2 = 3002 + 10x`.
- **Sonuç: `3002 + 10x`.**

<a id="ornek-7"></a>
## Örnek 7 — Katlı Denklemde Benzetme ile Bölme

**Soru:** 3 basamaklı `4AB` sayısı, 2 basamaklı `AB` sayısının `17`
katıdır. `A × B` çarpımı kaçtır?

**Çözüm:**
- `AB = x` dersen: `4AB = 400 + x`.
- Denklem: `400 + x = 17x` → `400 = 16x` → `x = 25`.
- `AB = 25` → `A = 2, B = 5`.
- **Sonuç: `A × B = 2 × 5 = 10`.**

<a id="ornek-8"></a>
## Örnek 8 — İki Ayrı Katlı Şart ile Zincirleme Çözüm

**Soru:** İki basamaklı `AB` doğal sayısı, rakamları toplamının `5`
katına eşittir. İki basamaklı `AC` doğal sayısı, rakamları toplamının
`7` katına eşittir. `A + B + C` toplamı kaçtır?

**Çözüm:**
- `AB = 5(A+B)` → `10A + B = 5A + 5B` → `5A = 4B`. Rakam sınırları içinde
  bu eşitliği sağlayan tek çift: `A = 4, B = 5` (`5×4=20=4×5`).
- `AC = 7(A+C)` → `10A + C = 7A + 7C` → `3A = 6C` → `A = 2C`. `A = 4`
  olduğu için `C = 2`.
- `A + B + C = 4 + 5 + 2 = 11`.
- **Sonuç: `11` (C seçeneği).**

<a id="ornek-9"></a>
## Örnek 9 — Denklemi Ortak Değişkene İndirip En Büyük/En Küçüğü Bulma

**Soru:** 2 basamaklı `Pr` doğal sayısı, 2 basamaklı `1p` doğal
sayısının `r` katına eşittir (`p` ile `P` aynı rakam). `Pr` sayısının en
büyük değeri, en küçük değerinden kaç fazladır?

**Çözüm:**
- `Pr = 10P + r`, `1p × r = (10+P) × r = 10r + Pr` (çarpım).
- Denklem: `10P + r = 10r + P×r` → `10P = 9r + P×r` → `10P = r(9+P)`
  → `r = 10P / (P+9)`.
- **En büyük için** `P = 9` dene: `r = 90/18 = 5` → sayı `95`.
- **En küçük için** `P = 1` dene: `r = 10/10 = 1` → sayı `11`.
- Fark: `95 - 11 = 84`.
- **Sonuç: `84` (D seçeneği).**

<a id="ornek-10"></a>
## Örnek 10 — Çarpımı Dağıtarak Ondalık Sonucu Bulma

**Soru:** `ABC` 3 basamaklı bir doğal sayı, `X` bir reel sayıdır.
`A×X = 8,75`, `B×X = 2,5`, `C×X = 5` ise `ABC × X` nedir?

**Çözüm:**
- `ABC × X = 100(A×X) + 10(B×X) + (C×X)`
- `= 100 × 8,75 + 10 × 2,5 + 5`
- `= 875 + 25 + 5 = 905`.
- **Sonuç: `905` (E seçeneği).**

<a id="ornek-11"></a>
## Örnek 11 — Fark Denkleminden Çarpımı Maksimize Etme

**Soru:** Burcu'nun boyu `190 - AB`, Kerem'in boyu `190 - BA` cm'dir
(`AB`, `BA` iki basamaklı doğal sayılar). Burcu, Kerem'den `54` cm
uzundur. `A × B` çarpımı en çok kaçtır?

**Çözüm:**
- Fark: `(190-AB) - (190-BA) = BA - AB = 54`
- `BA - AB = 9(B - A) = 54` → `B - A = 6`.
- `B - A = 6`'yı sağlayan çiftlerden çarpımı en büyük olanı bulmak için
  dene: `(A,B)=(1,7)→7`, `(2,8)→16`, `(3,9)→27`.
- En büyük çarpım `A=3, B=9` iken elde edilir: `3×9 = 27`.
- **Sonuç: `27` (E seçeneği).**

<a id="ornek-12"></a>
## Örnek 12 — Basamak Artış/Azalışını Sayı Adediyle Çarpma

**Soru:** 3 basamaklı 5 doğal sayının her birinin yüzler basamağı `3`
artırılıp, onlar ve birler basamağı `2`'şer azaltılıyor. Bu sayıların
toplamı kaç artar?

**Çözüm:**
- Tek bir sayı için etki: yüzler `+3` → `+300`; onlar `-2` → `-20`;
  birler `-2` → `-2`.
- Tek sayı için net artış: `300 - 20 - 2 = 278`.
- `5` sayı için: `278 × 5 = 1390`.
- **Sonuç: `1390` artar.**

<a id="ornek-13"></a>
## Örnek 13 — Çarpımın Basamak Sayısı Aralığını Bulma

**Soru:** 5 basamaklı bir doğal sayı ile 7 basamaklı bir doğal sayı
çarpılıyor. Çarpım en az kaç, en çok kaç basamaklı olur?

**Çözüm:**
- Kural: `a` basamaklı × `b` basamaklı çarpım en çok `a+b`, en az
  `a+b-1` basamaklıdır.
- `a=5, b=7` → en çok `5+7=12` basamaklı, en az `12-1=11` basamaklı.
- **Sonuç: en çok `12`, en az `11` basamaklı.**

<a id="ornek-14"></a>
## Örnek 14 — Katlı Denklemi Çözüp Rakamları Toplama

**Soru:** İki basamaklı `mn` doğal sayısının onlar basamağındaki rakam
`4` artırılıp, birler basamağındaki rakam `2` azaltıldığında oluşan iki
basamaklı sayı, `mn` sayısının 2 katına eşittir. `m + n` kaçtır?

**Çözüm:**
- Onlar basamağı `4` artınca sayı `+40` artar; birler basamağı `2`
  azalınca sayı `-2` azalır. Yeni sayı: `mn + 40 - 2 = mn + 38`.
- Denklem: `mn + 38 = 2 × mn` → `mn = 38`.
- `m = 3, n = 8` → `m + n = 11`.
- **Sonuç: `11` (B seçeneği).**

<a id="ornek-15"></a>
## Örnek 15 — Yanlış Okunan Rakamın Etkisini İki Yöntemle Bulma

**Soru:** Ali, bir `x` sayısını `35` ile çarpmış ve sonucu `840`
bulmuştur. Ancak işlemi kontrol ettiğinde, `x` sayısının aslında `6`
olan onlar basamağını `2` olarak gördüğünü fark etmiştir. İşlemin doğru
sonucu nedir?

**Çözüm (1. yol — doğrudan):**
- `840 / 35 = 24` → Ali'nin (yanlış) bulduğu `x` sayısı `24`'tür.
- Onlar basamağındaki `2`, gerçekte `6` olmalı → doğru `x = 64`.
- `64 × 35 = 2240`.

**Çözüm (2. yol — fark yöntemi):**
- Yanlış görülen rakam ile doğru rakam farkı: `6 - 2 = 4`; bu, onlar
  basamağında olduğu için sayıya etkisi `40`'tır (`x`'i `40` eksik
  görmüş).
- Bu `40` eksiklik, `35` ile çarpıldığı için sonuca `40 × 35 = 1400`
  eksik yansımıştır.
- Doğru sonuç: `840 + 1400 = 2240`.
- **Sonuç: `2240` (E seçeneği).**

<a id="ornek-16"></a>
## Örnek 16 — Toplamı Sabit Sayı Grubunda En Küçüğü Minimize Etme

**Soru:** Birbirinden farklı, 2 basamaklı 6 doğal sayıdan ikisi `60`'tan
küçüktür. Bu 6 doğal sayının toplamı `472` olduğuna göre, sayıların en
küçüğü en az kaç olabilir?

**Çözüm:**
- En küçük sayıyı minimize etmek için diğer sayıları mümkün olduğunca
  büyük seç: 2 basamaklının en büyükleri `99, 98, 97, 96` (4 tanesi
  `60`'tan büyük olabilir).
- `60`'tan küçük olması gereken ikinci sayı da mümkün olduğunca büyük
  seçilir: `59`.
- Bu 5 sayının toplamı: `99+98+97+96+59 = 449`.
- Kalan (en küçük) sayı: `472 - 449 = 23`.
- **Sonuç: `23` (A seçeneği).**

<a id="ornek-17"></a>
## Örnek 17 — Hatalı Kaydırılmış Çarpım Toplamından Geri Gitme

**Soru:** Bir çarpma işleminde iki ara çarpım (1. çarpım ve 2. çarpım)
hatalı kaydırma nedeniyle alt alta gelmiş ve toplamları `357`
bulunmuştur. 1. çarpım `3 × AB`, 2. çarpım `4 × AB` biçimindedir. 1.
çarpım olarak gösterilen sayı nedir?

**Çözüm:**
- `3×AB + 4×AB = 7×AB = 357` → `AB = 51`.
- 1. çarpım `3 × AB = 3 × 51 = 153`.
- **Sonuç: `153`.**

<a id="ornek-18"></a>
## Örnek 18 — Sütun Toplamada Elde Zinciriyle Rakam Bulma

**Soru:** Alt alta yazılmış bir toplama işleminde `A`, `B`, `C` birer
rakamdır. Sütun toplamlarından (elde vererek) `A + B + C` toplamı
bulunacaktır.

**Çözüm:**
- Birler basamağından başla: sütun toplamı `9`'u geçtiği için bir üst
  basamağa **elde `1`** gider; bu, o sütundaki bilinmeyen rakamı (`B`)
  belirler.
- Onlar basamağında, elde gelen `1` ile birlikte toplam yine `9`'u
  geçtiği için bir üst basamağa tekrar **elde `1`** gider; bu da ikinci
  bilinmeyeni (`A`) belirler.
- Yüzler basamağında kalan elde, üçüncü rakamı (`C`) tamamlar.
- Zincirleme çözümde: `A = 6`, `B = 4`, `C = 1`.
- `A + B + C = 6 + 4 + 1 = 11`.
- **Sonuç: `11` (B seçeneği).**

<a id="ornek-19"></a>
## Örnek 19 — Sütun Çıkarmada Ödünç Alma Zinciriyle Rakam Bulma

**Soru:** Alt alta yazılmış bir çıkarma işleminde `A4B - C1 = B89`
biçiminde bir eşitlik verilmiştir. `A + B + C` toplamı kaçtır?

**Çözüm:**
- Birler basamağından başla: üstteki rakamdan alttaki çıkarılınca sonuç
  `9` gelmesi için **komşudan `10`luk ödünç alınması** gerekir; bu,
  `B`'yi belirler (`B = 0`).
- Ödünç verilen basamakta bir azalma olur; bu azalmayla birlikte onlar
  basamağındaki çıkarma da **ödünç almayı** gerektirir; bu da `A`'yı
  belirler (`A = 5`).
- Kalan basamaktan `C` bulunur (`C = 4`).
- `A + B + C = 5 + 0 + 4 = 9`.
- **Sonuç: `9` (A seçeneği).**

<a id="ornek-20"></a>
## Örnek 20 — Boş Basamaktan İki İhtimali Eleyerek Rakam Bulma

**Soru:** Alt alta yazılmış bir çıkarma işleminde `A`'dan `B` çıkınca
`B` kalıyor, `A`'dan `3` çıkınca sonuç görünmüyor (boş/`0`). Buna göre
`A + B` toplamı kaçtır?

**Çözüm:**
- Boş basamak `0` anlamına geldiği için iki ihtimal var: `A = 3` (ödünç
  almadan) ya da `A = 4` (komşudan ödünç alınarak `13 - 3 = 0`).
- `A = 3` denenir: `3 - B = B` → `2B = 3`, tam sayı çözüm yok → **elenir**.
- `A = 4` denenir: ödünç almadan `4 - B = B` → `2B = 4` → `B = 2`;
  ödünçle `14 - B = B` → `2B = 14` → `B = 7`. İki olasılık da denenir,
  sağlama yapılınca yalnızca `B = 7` diğer sütunlarla tutarlı çıkar.
- `A = 4, B = 7` → `A + B = 11`.
- **Sonuç: `11` (C seçeneği).**

<a id="ornek-21"></a>
## Örnek 21 — Rakam Çiftleştirme ile Toplamı 999 Yapan Sayıları Bulma

**Soru:** `2, 3, 4, 5, 6, 7` rakamlarından 3 tanesiyle 3 basamaklı `mnp`
sayısı, kalan 3 tanesiyle de `rst` sayısı oluşturuluyor. `mnp + rst =
999` olduğuna göre aşağıdakilerden hangisi `rst` sayısı **olamaz**?

**Çözüm:**
- Toplamın her basamağı `9` etmesi için (elde olmadan), her basamak
  çiftinin toplamı `9` olmalı. Verilen 6 rakam içinde toplamı `9` eden
  çiftler: `(2,7)`, `(3,6)`, `(4,5)`.
- Bu üç çiftin her biri, **biri `mnp`'de biri `rst`'de** olacak şekilde
  dağıtılmalı; aynı çiftin iki üyesi aynı sayının içinde olursa o
  sayının rakamları toplamı `9` içeren bir çift barındırır ama karşı
  sayıda eşleşen rakam kalmaz, dolayısıyla toplam `999` olamaz.
- `263`, `345`, `452`, `723` gibi seçenekler, bir çiftin iki üyesini
  birden barındırdığı için **olamaz**.
- Geçerli tek dağıtım: `mnp = 347`, `rst = 652` (`347+652=999` ✓).
- **Sonuç: geçerli `rst = 652`; çiftin iki üyesini birden içeren
  seçenekler `rst` olamaz.**

<a id="ornek-22"></a>
## Örnek 22 — Mantık Sorusunda Olasılık Sayısını Karşılaştırma

**Soru:** Sezen, aklından 2 basamaklı bir sayı tutuyor: asal, `50`'den
küçük, rakamlarından biri `7`, rakamlarından biri `8`. Verilen 4
bilgiden biri yanlış, üçü doğru. Feridun, bu sayıyı kesinlikle tahmin
edebilmesi için en az kaç tahminde bulunmalıdır?

**Çözüm:**
- "Rakamlarından biri `8`" bilgisi doğru kabul edilirse, sayı `18, 28,
  38, 48` gibi bir **çift sayı** olmak zorunda kalır; çift sayılar `2`
  hariç asal olamaz → bu bilgiyle "asaldır" bilgisi çelişir. Demek ki
  **yanlış olan bilgi budur** ("rakamlarından biri `8`").
- Geri kalan doğru bilgiler (asal, `50`'den küçük, rakamlarından biri
  `7`) sağlanan sayılar: `17, 37, 47` (hepsi asal, `50`'den küçük, biri
  `7`).
- `3` olasılık olduğu için Feridun, kesin tahmin için en az `3`
  tahminde bulunmalıdır (ilk ikisi yanlış çıksa bile üçüncüsü kesin
  doğru olur).
- **Sonuç: en az `3` tahmin.**

<a id="ornek-23"></a>
## Örnek 23 — İki Kare Farkı Kimliğiyle Çarpımı Çözme

**Soru:** Rakamları farklı, 2 basamaklı `AB` doğal sayısı için, "daire
içinde `AB`" ifadesi `AB - BA` olarak, "üçgen içinde `AB`" ifadesi
`A² - B²` olarak tanımlanıyor. Bu ikisinin çarpımı `45` ise, `AB`
sayısının rakamları çarpımı kaçtır?

**Çözüm:**
- `AB - BA = 9(A - B)`.
- `A² - B² = (A-B)(A+B)` (iki kare farkı).
- Çarpım: `9(A-B) × (A-B)(A+B) = 9(A-B)²(A+B) = 45` → `(A-B)²(A+B) = 5`.
- `5` asal olduğu için tek çarpanlara ayırma biçimi `1 × 1 × 5`:
  `(A-B)² = 1` → `A - B = 1`; `A + B = 5`.
- İki denklemi çöz: `A = 3, B = 2`.
- **Sonuç: rakamlar çarpımı `3 × 2 = 6`.**

<a id="ornek-24"></a>
## Örnek 24 — Çift Yönlü Eşitsizlikten Rakam Eşitliği Çıkarma

**Soru:** 2 basamaklı `AB` ve `BA` sayıları için bir görselde hem
`(bir taraf) < AB` hem `AB < (başka bir taraf)` biçiminde çapraz
eşitsizlikler verilmiş; sıralamalardan hangisi doğrudur?

**Çözüm:**
- Eğer aynı anda hem `AB < BA` hem `BA < AB` biçiminde bir durum ortaya
  çıkıyorsa (görseldeki karşılaştırmalarda), bu ancak `A = B` ise
  çelişkisiz sağlanabilir; çünkü iki farklı rakamlı sayı, karşılıklı
  olarak birbirinden hem büyük hem küçük olamaz.
- `A = B` kabul edilince `AB` ile `BA` aynı sayı olur, karşılaştırma
  sadeleşir ve geriye kalan basamaklardaki (`C`, `D` gibi) rakamlar
  sıralamayı belirler.
- Ortaya çıkan doğru sıralama: **`C < A = B < D`**.
- **Sonuç: `C < A = B < D`.**

<a id="ornek-25"></a>
## Örnek 25 — Örüntüden Formüle Geçerek Kısa Yoldan Rakam Toplamı Bulma

**Soru:** Tüm basamakları `1` olan bir doğal sayının karesi alınıyor
(`1²=1`, `11²=121`, `111²=12321`, ...). Tüm basamakları `1` olan `8`
basamaklı bir sayının karesi alındığında, sonucun rakamları toplamı
kaçtır?

**Çözüm (örüntü yoluyla):**
- `n` basamaklı "hepsi `1`" bir sayının karesi, ortadan `n`'e kadar
  yükselip simetrik inen bir basamak dizisi oluşturur
  (`1,2,3,...,n,...,3,2,1`, `n ≤ 9` için geçerli).
- `8` basamaklı için dizi: `1,2,3,4,5,6,7,8,7,6,5,4,3,2,1`.
- Rakamları toplamı: `1'den 7'ye kadar toplam × 2 + 8 = 28×2+8 = 64`.

**Çözüm (kısa yoldan — örüntü formülü):**
- Gözlemlenen kural: `n` basamaklı "hepsi `1`" sayının karesinin
  rakamları toplamı doğrudan `n²`'ye eşittir (`1²=1`, `2²=4`, `3²=9`, ...).
- `n = 8` için: `8² = 64`.
- **Sonuç: `64`.**

<a id="ornek-26"></a>
## Örnek 26 — Kibrit Çöpü Kısıtıyla En Büyük Sayıyı Oluşturma

**Soru:** Kibrit çöpleriyle rakam oluşturmak için standart çöp sayıları
kullanılıyor (bkz. Teorik Bilgiler'deki tablo). `14` kibrit çöpü
kullanılarak, rakamları birbirinden farklı, 4 basamaklı yazılabilecek en
büyük doğal sayı yazılacaktır. Bu sayının birler ve yüzler
basamağındaki rakamların toplamı kaçtır?

**Çözüm:**
- En büyük 4 basamaklı farklı rakamlı sayı `9876` olurdu, ama çöp
  maliyeti (`6+7+3+6=22`) `14`'ü aşar; `9` ile başlamak da denendiğinde
  kalan `8` çöple diğer 3 rakam tamamlanamaz.
- `7` ile başlamayı dene (`3` çöp, kalan `11` çöp): `6`'yı eklemek
  (`6` çöp) dener ama kalan `5` çöple ikinci ve üçüncü rakamı
  tamamlamak (gereken kombinasyonlar `7` zaten kullanıldığı için)
  mümkün olmuyor → `6` elenir.
- `5`'i dene (`5` çöp, toplam `7+5=8` çöp, kalan `6` çöp): kalan `6`
  çöple iki farklı rakam bulunmalı → `4` (`4` çöp) ve `1` (`2` çöp)
  toplamda `6` çöp eder ve en büyük sırayı vermek için `4` üçüncü,
  `1` son sıraya yazılır.
- Oluşan en büyük sayı: `7541` (çöp toplamı: `3+5+4+2=14` ✓).
- Birler basamağı `1`, yüzler basamağı `5`; toplamları: `1 + 5 = 6`.
- **Sonuç: `6` (A seçeneği).**

<a id="ornek-27"></a>
## Örnek 27 — Eşit Çarpım Çiftlerini Bulup Yer Değişimlerini Sayma

**Soru:** `2, 3, 4, 6, 8` rakamları birer kez kullanılarak 5 basamaklı
`ABCDE` sayıları yazılacaktır; `A × B = D × E` koşulunu sağlayan kaç
farklı `ABCDE` sayısı yazılabilir?

**Çözüm:**
- Verilen 5 rakam içinden birbirine eşit çarpım üreten ikili grupları
  bul: `2×6=12` ve `3×4=12` (eşit); `3×8=24` ve `6×4=24` (eşit). Diğer
  kombinasyonlar eşleşmiyor.
- Her eşit-çarpım grubunda kullanılmayan tek rakam, ortadaki `C`
  basamağına sabitlenir.
- Bir grup için: `(A,B)` ikilisi kendi içinde `2` farklı sırada
  yazılabilir, `(D,E)` ikilisi de `2` farklı sırada; ayrıca hangi ikili
  `AB` tarafında hangi ikili `DE` tarafında olacağı da `2` farklı
  şekilde seçilebilir → toplam `2×2×2 = 8` farklı sayı.
- İki grup olduğu için: `8 × 2 = 16`.
- **Sonuç: `16` farklı sayı yazılabilir.**

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

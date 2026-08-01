# 📘 Teorik Bilgiler — basamak kavramı

> Kaynak: Değişmeyen matematik kuralları (tanımlar, kurallar, formüller). Hoca anlatımından bağımsızdır.

## Basamak Değeri ve Sayı Değeri

Bir doğal sayıdaki her rakamın iki farklı değeri vardır:

- **Sayı değeri:** Rakamın kendisidir (bulunduğu yerden bağımsız).
- **Basamak değeri:** Rakamın, bulunduğu basamakla (birler=1, onlar=10,
  yüzler=100, ...) çarpılmasıyla elde edilen değerdir.

Örnek: `237` sayısında `2`'nin sayı değeri `2`, basamak değeri `200`'dür
(çünkü yüzler basamağındadır).

## Çözümleme (Harfli Açılım)

**Çözümleme**, bir doğal sayıyı oluşturan rakamların, bulundukları
basamağın değeriyle çarpılıp toplanması işlemidir. Harfli sayılarda da
aynı mantık uygulanır:

```
AB (2 basamaklı)  = 10×A + 1×B
ABC (3 basamaklı) = 100×A + 10×B + 1×C
ABCD (4 basamaklı) = 1000×A + 100×B + 10×C + 1×D
```

Genel kural: sağdan sola doğru basamak değerleri `1, 10, 100, 1000, ...`
şeklinde `10` katları olarak artar; her rakam bulunduğu basamağın
değeriyle çarpılır.

## Klasik Çözümleme Kalıpları

Sıkça karşılaşılan harfli ifadeler, çözümleme yapılıp sadeleştirildiğinde
aşağıdaki sabit kalıplara indirgenir (`A`, `B`, `C` birer rakamdır):

| İfade | Sadeleşmiş Hali |
|---|---|
| `AB + BA` | `11 × (A + B)` |
| `AB - BA` (A > B) | `9 × (A - B)` |
| `ABC - CBA` (A > C) | `99 × (A - C)` |
| `ABC + BCA + CAB` (aynı 3 rakamın çevrimsel permütasyonlarının toplamı) | `111 × (A + B + C)` |

Bu kalıplar ezberlenmese de, çözümleme + parantezine alma adımlarıyla her
seferinde yeniden türetilebilir; sınavda hız kazandıran, bu türetme
alışkanlığıdır.

## Basamak Değeri Değişim Kuralı

Bir sayının belirli bir basamağındaki rakam `k` kadar artırılır veya
azaltılırsa, sayının kendisi de o basamağın **basamak değeri kadar katı**
oranında artar veya azalır:

```
yüzler basamağı k artarsa  → sayı 100k artar
onlar basamağı  k artarsa  → sayı 10k artar
birler basamağı k artarsa  → sayı 1k artar
```

Bu kural, birden fazla basamakta aynı anda değişiklik olduğunda her
basamağın etkisi ayrı ayrı hesaplanıp toplanarak/çıkarılarak uygulanır.

## Benzetme (Sayının Bir Parçasını Değişkenle Gösterme)

**Benzetme**, çözümlemenin uzun sürdüğü durumlarda bir sayının bir kısmını
doğrudan bir değişkenle (örn. `x`) göstermeyi ifade eder. İki türü vardır:

- **Baştan benzetme:** Sayının baş tarafındaki rakam(lar) çıkarılınca
  geri kalan kısım aynen yazılır. Örn. `4BC` sayısında `4`'ü çıkarınca
  geriye `BC` kalır; sayı `400 + BC` şeklinde yazılabilir.
- **Sondan benzetme:** Sayının **son rakamı** çıkarılınca, çıkarılan
  rakamın yerinde `0` kalır. Bu `0` ile biten sayı, `10` (iki basamak
  çıkarıldıysa `100`, üç basamak çıkarıldıysa `1000`, ...) ile çarpılmış
  bir sayı olarak yazılabilir. Örn. `AB4` sayısında `4`'ü çıkarınca
  geriye `AB0` kalır; `AB0`'ın son rakamı `0` olduğu için bu `10 × AB`
  şeklinde yazılabilir, dolayısıyla `AB4 = 10×AB + 4`.

Genel kural: bir sayının **sonundaki `0` sayısı**, o sayının `10`'un
kaçıncı kuvvetiyle çarpılmış olduğunu gösterir (`1` tane `0` → `×10`,
`2` tane `0` → `×100`, ...).

## Rakam ve Basamak Kısıtları

- Bir **rakam**, `0`'dan `9`'a kadar (dahil) tam sayı değeri alabilir;
  bunun dışında değer alamaz.
- Bir sayının **en soldaki (baş) rakamı `0` olamaz** — aksi hâlde sayı,
  iddia edilen basamak sayısında olmaz. Örneğin `AB` iki basamaklı bir
  sayıysa, `A ≠ 0` olmak zorundadır; ama `B = 0` olabilir.
- Soru metninde harflerin **"birbirinden farklı"** olduğu açıkça
  belirtilmemişse, farklı harflerin aynı rakama karşılık gelmesi
  (örn. `A = B`) matematiksel olarak geçerlidir; harflere farklı değerler
  vermek zorunlu değildir.

## İki Sayının Çarpımının Basamak Sayısı Kuralı

`a` basamaklı bir doğal sayı ile `b` basamaklı bir doğal sayının çarpımı:

```
en fazla (a + b) basamaklı olur
en az    (a + b - 1) basamaklı olur
```

(En büyük durumu görmek için her iki sayıyı da kendi basamak sayısında
en büyük rakamlarla — örn. `999 × 99` — en küçük durumu görmek için de
en küçük rakamlarla — örn. `100 × 10` — denemek bu kuralı doğrular.)

## Kibrit Çöpü (Dijital Gösterge) Rakam-Çöp Sayısı Tablosu

DGS'de bazı ÖSYM tarzı sorularda, rakamların bir dijital gösterge
(7 parçalı ekran) üzerinde kaç çöp/çizgi ile oluşturulduğu verilir.
Standart tablo şu şekildedir:

| Rakam | Çöp Sayısı |
|---|---|
| 0 | 6 |
| 1 | 2 |
| 2 | 5 |
| 3 | 5 |
| 4 | 4 |
| 5 | 5 |
| 6 | 6 |
| 7 | 3 |
| 8 | 7 |
| 9 | 6 |

Bu değerler soruda ayrıca verilmese bile, sorunun çözümü sırasında
kullanılan sayılarla tutarlılığı kontrol edilerek doğrulanabilir.

[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)

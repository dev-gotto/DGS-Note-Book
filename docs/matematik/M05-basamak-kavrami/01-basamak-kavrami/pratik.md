# 💡 Pratik Bilgiler — basamak kavramı

> Kaynak: Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## Çözümlemeyi Kafadan Hızlı Yazma Yöntemi

Harfli bir sayıyı çözümlerken kağıda yazılı formül ezberlemek yerine, her
rakama tek tek "bu hangi basamakta?" diye sorup basamak değerini
doğrudan yazmak daha hızlıdır. Örneğin `ABA` gibi bir sayıda ilk `A`
yüzler basamağında (`100A`), ikinci `A` birler basamağında (`1A`) olduğu
için ikisi toplanır (`101A`); sonra `B` onlar basamağında (`10B`) ayrı
yazılır. Bu, sayıyı tek seferde parçalamak yerine **her rakamı kendi
basamağına göre ayrı ayrı okuma** alışkanlığıdır.

## Çözümleme Sonrası "Değer Verme" Stratejisi

Çözümleme yapılıp rakamlar arasındaki toplam/fark/ilişki bulunduktan
sonra, soru genellikle "en büyük/en küçük kaçtır", "kaç farklı sayı
vardır" gibi bir devamla biter. Bu noktada yapılacak şey **değer
vermektir**: bulunan ilişkiyi sağlayan rakamlara (0-9 aralığında, baş
rakam ≠ 0 kısıtına dikkat ederek) uygun değerler denenir. "Hak ettiği
kadar" değer verilir — yani rakamın alabileceği en büyük/en küçük sınır
her zaman `9`/`0` (baş rakamda `1`) olur, bu sınırın ötesine geçilmez.

## Benzetme Ne Zaman Kullanılır

Çözümleme, ifadedeki harf/rakam sayısı arttıkça uzayıp karmaşıklaşabilir.
Böyle durumlarda **benzetme** tercih edilir: ifadenin tekrar eden bir
parçası (örn. iki basamaklı `AB` bloğu) doğrudan `x` gibi bir değişkenle
gösterilir, geri kalan sabit kısım normal çözümlemeyle yazılır. Bu,
işlemi tek adımda bitirmeyi sağlar ve büyük sayılarla uğraşmayı önler.

## Baştan Benzetme Uygulaması

Sayının **baş tarafındaki** rakam(lar) çıkarılır, kalan kısım olduğu gibi
yazılır, çıkarılan rakamın basamak değeri ayrı eklenir. Örnek: `2AB`
sayısında `2`'yi çıkarırsan geriye `AB` kalır; `AB = x` dersen sayı
`200 + x` olur.

## Sondan Benzetme Uygulaması

Sayının **son rakamı** (veya son birkaç rakamı) çıkarılır; çıkarılan
rakamın yerine `0` gelir ve geriye kalan `...0` biçimindeki sayı, `10`
(veya `100`, `1000`...) ile çarpılmış hâliyle yazılır. Örnek: `3AB2`
sayısında `AB`'yi çıkarırsan geriye `3002` kalır (`AB`'nin yerine `0`
gelir: `30 0 2`); `AB = x` dersen sayı `3002 + 10x` olur (`AB0` sonu `0`
olduğu için `10 × AB` = `10x`).

## Basamak Artış/Azalışının Sayıya Etkisini Hızlı Hesaplama

Birden fazla basamakta aynı anda değişiklik olan sorularda, her basamağın
etkisini ayrı ayrı hesaplayıp topla/çıkar:

```
yüzler basamağı k artar  → +100k
onlar basamağı  m azalır → -10m
birler basamağı n azalır → -1n
toplam etki = 100k - 10m - 1n
```

Birden fazla sayı için soruluyorsa (örn. "5 sayının toplamı ne kadar
artar"), tek bir sayı için bulunan etki, sayı adediyle çarpılır.
Alternatif olarak, şartlara uygun **rastgele somut bir sayı seçip**
değişikliği o sayı üzerinde uygulamak ve farkı gözlemlemek de aynı
sonucu verir — bazı öğrenciler için bu yöntem daha kolay anlaşılır.

## Çarpım Basamak Sayısı Kuralının Pratik Kullanımı

"En çok/en az kaç basamaklı olur" tipi sorularda kuralı doğrudan uygula:
`a` basamaklı ile `b` basamaklı sayının çarpımı en çok `a+b`, en az
`a+b-1` basamaklıdır. Kanıtlamak istersen: en büyük durumu görmek için
her iki sayıyı da o basamak sayısındaki **en büyük** değerle (`999×99`
gibi), en küçük durumu görmek için de **en küçük** değerle (`100×10`
gibi) dene.

## 4 İşlem Sorularında Elde Verme-Alma ile Yorumlama

Toplama/çıkarma işlemi harfli olarak alt alta verildiğinde çözümleme
gerekmez; sütun sütun **elde alma/verme mantığıyla** yorumlanır:

- Bir sütunun toplamı `9`'u geçiyorsa, bir üst sütuna **elde `1`**
  gönderilir.
- Bir çıkarmada üstteki rakam alttakinden küçükse, komşu (bir üst)
  basamaktan **`10`luk ödünç alınır**, o basamak `1` azaltılır.
- Her sütunda "bu rakamla bu rakamı toplarsam/çıkarırsam sonuç ne olur,
  elde var mı yok mu" sorusu tek tek sorularak harfler tespit edilir.

## Yanlış Okunan Rakamın Sonuca Etkisini Bulma Yöntemi

Bir çarpma/toplama işleminde bir sayının **bir basamağı yanlış okunmuş**
ve doğru sonucun bulunması isteniyorsa, iki yol vardır:

1. **Doğrudan yol:** Yanlış işlemden yanlış çarpanı bul (bölme yaparak),
   o çarpanda yanlış okunan rakamı doğrusuyla değiştir, işlemi yeniden
   yap.
2. **Fark yolu:** Yanlış okunan rakamla doğru rakam arasındaki farkı,
   bulundukları basamağın değeriyle çarp; bu, diğer çarpanla da çarpılıp
   yanlış sonuca eklenir/çıkarılır. Bu yol, ilk yoldan daha az işlem
   gerektirir çünkü sayıyı yeniden bulmaya gerek kalmaz.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

# 💡 Pratik Bilgiler — ardışık sayılar

> Kaynak: Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## Fark Sorulduğunda Sayı Kullan, Harf Kullanma

Soru, ardışık sayıların **farkıyla ilgili bir şey** soruyorsa (harflerin
kendisini değil, aralarındaki bir farkı/ilişkiyi soruyorsa), harflerin
yerine dizinin türüne uygun **küçük, kullanışlı sayılar** yerleştirip
doğrudan işlem yapılabilir (ör. ardışık çift sayı için `2, 4, 6`). Sonuç,
hangi ardışık üçlüyü seçtiğine bağlı olarak değişmez, çünkü fark her
zaman sabittir.

**Ama dikkat:** Soru harflerin **kendisini** (sayı değerlerini)
soruyorsa, bu kısayol kullanılamaz — o zaman fark bilgisini cebirsel bir
ilişki kurmak için kullanmak gerekir (aşağıya bak).

## Fark Bilgisini Cebirsel Kısayol Olarak Kullan

Bir soru, sıralı ardışık sayılardan ikisinin farkını veriyorsa (ör.
`a - c = 23`) ve sonra başka iki terimin farkını soruyorsa, her terimi
`x`, `x+2`, `y`, `y+2` gibi ayrı ayrı harflerle ifade edip uzun bir
denklem kurmaya **gerek yoktur**. Bunun yerine, istenen farkı doğrudan
verilen farkın cinsinden ifade edecek şekilde harfleri sadeleştirmek çok
daha hızlıdır (bkz. Strateji sayfasındaki Örnek 1).

## Terim Sayısını Bulma Kısayolu

```
Terim Sayısı = (Son Terim − İlk Terim) / Artış Miktarı + 1
```

Artış miktarı `1` ise (birer birer giden bir aralık, ör. `61`'den
`82`'ye kaç sayı var), bölme adımına gerek yoktur — doğrudan
`Son − İlk + 1` hesaplanır.

## Ortadaki Sayıyı Bulma Kısayolu

- **Toplam biliniyorsa:** `Toplam / Terim Sayısı` ortadaki sayıyı verir.
- **Toplam bilinmiyorsa:** `(İlk Terim + Son Terim) / 2` ortadaki sayıyı
  verir (aritmetik ortalama).

## Tek Terim Sayılı Gruplarda Doğrudan Ortadaki Sayıdan Git

Terim sayısı tek olan bir ardışık grup toplamı verildiğinde (ör.
"ardışık 7 tek sayının toplamı 105"), sayıları `x, x+2, x+4...` gibi tek
tek yazıp toplayıp `x`'i çözmek **uzun ve gereksizdir.** Bunun yerine:
toplamı terim sayısına böl → ortadaki sayıyı bul → istenen sayıya
(en küçük, en büyük vb.) ortadaki sayıdan adım adım ilerleyerek ulaş.

## Çift Terim Sayılı Gruplarda "Aradaki Sayı" Kavramını Kullan

Terim sayısı çift olduğunda gerçek bir "ortadaki sayı" yoktur; bunun
yerine iki orta terimin ortalaması olan **"aradaki sayı"** aynı rolü
üstlenir (`Toplam / Terim Sayısı` formülü yine geçerlidir, sadece çıkan
sayı dizinin gerçek bir üyesi olmayabilir).

## 1'den Başlamayan Bir Aralığın Toplamını Bulma

Toplam `1`den değil de başka bir sayıdan başlıyorsa (ör. `5`'ten
`19`'a kadar), aralığı `1`den başlıyormuş gibi düşünüp, **`1`den son
sayıya kadar olan toplamdan, `1`den (ilk sayının bir öncesine) kadar olan
toplamı çıkararak** bulabilirsin:

```
İstenen Toplam = (1'den Son Sayıya Kadarki Toplam) − (1'den İlk Sayının Bir Öncesine Kadarki Toplam)
```

## Her Terim Sabit Bir Miktar Artırılırsa Toplam Ne Kadar Artar

Bir ardışık sayı toplamındaki **her terim** sabit bir miktar (ör. `5`)
artırılırsa, yeni toplam eskisinden şu kadar artar:

```
Toplamdaki Artış = Terim Sayısı × Terim Başına Artış Miktarı
```

Sayıları tek tek artırıp yeniden toplamaya gerek yoktur.

## Çarpımsal Terimli Toplamlarda "Sabit Çarpanı Sil" Kısayolu

`1×2 + 2×3 + 3×4 + ...` gibi çarpımsal terimlerden oluşan bir toplamda,
yalnızca **bir terimin çarpanı** (ör. ikinci çarpan) sabit bir miktar
artırılıyorsa:

1. **Değişmeyen çarpanı(ları) sil** — sadece değişen çarpanlarla oluşan
   yeni bir ardışık sayı dizisi kalır.
2. Bu yeni dizinin toplamını (`terim sayısı × ortadaki sayı` ile) bul.
3. Bulduğun toplamı, terimin **arttığı miktarla** çarp — bu, toplamdaki
   toplam artışı verir.

Bu yöntem, her terimi tek tek yeniden çarpıp eski toplamdan çıkarmaktan
çok daha hızlıdır (bkz. Strateji sayfasındaki ilgili örnek).

## Yanlışlıkla Çıkarma Yapılan Terimi Bulma

Bir dizi sayı toplanırken bir terimin önüne yanlışlıkla `+` yerine `-`
konursa, bu terim hem toplanmamış hem de fazladan bir kez çıkarılmış
olur. Bu yüzden:

```
Doğru Toplam − Yanlış Toplam = 2 × (Eksi Konan Terim)
```

Doğru toplamı (genelde standart formülle) hesapla, yanlış sonuçla
karşılaştır, farkı `2`ye böl — yanlışlıkla eksi konan terimi bulursun.

## En Az / En Çok Değer Aralığında Ara Değerlerin Hepsi Alınabilir

Bir toplamın alabileceği en küçük ve en büyük değer bulunduğunda (ör.
bazı terimlere fazladan bir işlem yapılıp yapılmaması seçilebiliyorsa),
bu iki uç değer arasındaki **tüm tam sayı değerleri** de toplam
tarafından alınabilir. Bu yüzden "kaç farklı değer alabilir" sorularında
yalnızca `en büyük − en küçük + 1` hesaplamak yeterlidir.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

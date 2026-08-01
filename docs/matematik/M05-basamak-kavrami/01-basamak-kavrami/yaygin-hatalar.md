# ⚠️ Yaygın Hatalar — basamak kavramı

> Kaynak: Öğrencilerin sık yaptığı hatalar ve ÖSYM'nin kurduğu tuzaklar.
> Her madde; hata/tuzak örneği + derin kavrayışla çözümü şeklinde anlatılır.

## 1. Sondaki Sıfırı Önemsiz Sanmak, Baştaki Sıfırı Önemli Sanmak

**Hata:** Bir sayıdan bir rakam çıkarılıp benzetme yapılırken, çıkarılan
rakamın konumuna bakılmaksızın "geriye kalan `0`" her zaman göz ardı
edilir ya da her zaman yazılır.

**Neden yanlış:** Bir sayının **baştaki** `0`'ı değersizdir (yazılmaz),
ama **sondaki** `0`'ı değerlidir ve sayının büyüklüğünü doğrudan
etkiler (`25000` ile `250000` arasındaki fark tam olarak budur). Sondan
benzetme yaparken bu `0`'ı atlamak, `10`'un doğru kuvvetini kaçırmaya
sebep olur.

**Doğru çözüm:** Sondan benzetme yaptığında geriye kalan `...0`
biçimindeki sayının kaç tane sondan `0` içerdiğini say; bu, sayının `10`
un hangi kuvvetiyle çarpılmış olduğunu (`×10`, `×100`, ...) verir.

## 2. Harflerin Otomatik Olarak Farklı Rakam Olduğunu Varsaymak

**Hata:** Soru metninde "rakamlar birbirinden farklıdır" yazmadığı hâlde,
farklı harflerle gösterilen rakamlara otomatik olarak farklı değerler
verilir; bu yüzden en büyük/en küçük değer ararken bazı geçerli
çözümler (örn. `A = B`) gözden kaçırılır.

**Neden yanlış:** Harflerin görünüşte farklı olması (`A`, `B` gibi ayrı
sembollerle yazılması), matematiksel olarak farklı değer almaları
gerektiği anlamına gelmez. Soru açıkça belirtmedikçe bu bir kısıt
değildir.

**Doğru çözüm:** Soru metnini dikkatle oku; "farklı rakamlardır/farklı
sayılardır" ibaresi yoksa en büyük/en küçük değer ararken aynı rakamı
birden fazla harfe vermekten çekinme (bkz. Örnek 3 — `991` çözümünde
`B = 9` iken `A = 9` olabilmesi).

## 3. Çift Basamaklı Sayının Baş Rakamının `0` Olabileceğini Unutmamak

**Hata:** İki (veya daha fazla) basamaklı bir sayı için değer verirken,
en büyük/en küçük değer aranırken baş rakama `0` verilerek geçersiz bir
sayı (örn. `07`) üretilir.

**Neden yanlış:** Bir sayının basamak sayısı iddiası (`iki basamaklı`,
`üç basamaklı`), baş rakamının `0` olamayacağı anlamına gelir; baş
rakam `0` olursa sayı iddia edilenden daha az basamaklı olur.

**Doğru çözüm:** Değer verirken önce hangi harfin baş rakam olduğunu
belirle, ona asla `0` verme; sadece sondaki (birler, hatta onlar)
basamaktaki rakamlara `0` verilebilir (bkz. Örnek 2'de `B ≠ 0` kısıtı).

## 4. Basamak Değeri Artış/Azalışını Yanlış Katsayıyla Uygulamak

**Hata:** Bir basamaktaki rakam `k` kadar artırıldığında, sayıya olan
etkisinin doğrudan `k` olduğu düşünülür; basamağın konumuna göre
katsayı (`×1`, `×10`, `×100`, ...) çarpılmaz.

**Neden yanlış:** Bir basamaktaki değişikliğin sayıya etkisi, o
basamağın **basamak değeriyle** orantılıdır. Onlar basamağındaki `1`
birimlik bir değişiklik bile sayıyı `10` birim değiştirir.

**Doğru çözüm:** Her basamak değişikliğini kendi basamak değeriyle
çarparak hesapla, sonra hepsini topla/çıkar (bkz. Örnek 12'de yüzler
`×100`, onlar `×10`, birler `×1` ayrı ayrı çarpılıp toplanıyor).

## 5. Çözümleme Uzunken Benzetmeye Geçmeyi Akıl Edememek

**Hata:** Uzun/karmaşık harfli ifadelerde her rakamı tek tek çözümlemeye
devam edilir; işlem gereksiz yere uzar ve hata riski artar.

**Neden yanlış:** İfadede tekrar eden bir blok (iki veya üç basamaklı
bir alt-sayı) varsa, bu bloğu tek tek çözümlemek yerine bir değişkenle
göstermek işlemi ciddi ölçüde kısaltır; uzun çözümleme sırasında işlem
hatası yapma olasılığı artar.

**Doğru çözüm:** İfadede aynı blok birden fazla yerde geçiyorsa (örn.
`AB` iki basamaklı bloğu), o bloğu doğrudan `x` ile göster ve denklemi
bu değişken üzerinden kur (bkz. Örnek 7).

## 6. Sütun Toplama/Çıkarma Bulmacalarında Elde/Ödünç Zincirini Atlamak

**Hata:** Alt alta yazılmış harfli toplama/çıkarma sorularında, bir
sütunun sonucunu doğrudan görünen rakamdan okuyup, o sütundan bir üst
sütuna elde gidip gitmediği (veya bir üst sütundan ödünç alınıp
alınmadığı) kontrol edilmeden ilerlenir.

**Neden yanlış:** Görünen rakam, elde/ödünç etkisiyle **gerçek toplam/
fark sonucundan farklı** olabilir (örn. toplam `11` olduğunda görünen
rakam `1`'dir ama elde `1` bir üst basamağa gitmiştir). Bu adımı
atlamak yanlış rakam bulunmasına yol açar.

**Doğru çözüm:** Sütunlara birler basamağından başlayarak sırayla ilerle;
her sütunda "elde var mı", "ödünç almam gerekiyor mu" sorusunu mutlaka
sor ve bir sonraki sütuna bu bilgiyi taşı (bkz. Örnek 18, Örnek 19,
Örnek 20).

## 7. Mantık Sorularında Koşulu Sağlayan Sayı Sayısını Eksik Saymak

**Hata:** "Kaç kişi tahmin edemez", "en az kaç tahmin gerekir" gibi
mantık sorularında, aranan koşulu (örn. rakamları toplamı belli bir
sayı olan iki basamaklı sayılar) sağlayan sayı adedi eksik/yanlış
sayılır; bu da yanlış bir "en az tahmin sayısı" sonucuna götürür.

**Neden yanlış:** Bu tip sorularda cevap doğrudan **sistematik sayma**
işlemine dayanır; rastgele birkaç örnek yazıp "galiba bu kadar" demek,
sınır durumlardaki (örn. bir rakamın `0` olabildiği) sayıları
kaçırmaya sebep olur.

**Doğru çözüm:** Koşulu sağlayan tüm sayıları küçükten büyüğe (veya
büyükten küçüğe) sistematik olarak listele, `0` dahil sınır rakamları
atlamadığından emin ol, sonra say (bkz. Örnek 22'de `50`den küçük asal
sayı listesi).

[← Konu ana sayfasına dön](index.md) · [Hızlı Tekrar →](hizli-tekrar.md)

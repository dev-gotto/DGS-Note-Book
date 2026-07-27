# 💡 Pratik Bilgiler — Sayı Kümeleri

> Kaynak: Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## Rakamlarla Kurulan İfadelerde En Büyük/En Küçük Değer

Bir ifadenin en küçük/en büyük değerini bulurken **katsayısı büyük olan
harfe önce karar verilir**:

- İfadeyi **küçültmek** istiyorsan, çıkarılan (negatif katsayılı) terimin
  harfine **en büyük rakamı**, toplanan (pozitif katsayılı) terimlerin
  harflerine **en küçük rakamları** ver.
- İfadeyi **büyütmek** istiyorsan bu mantığın tam tersini uygula.
- Harfler için "birbirinden farklı rakamlar" **denmediği sürece** aynı
  değer de verilebilir.

## Sayı Türünün Önemi

En büyük/en küçük değer sorularında **sayı türü mutlaka dikkatle
okunmalıdır**, çünkü kullanılabilecek en küçük değer türe göre değişir:

- **Doğal sayı** deniyorsa en küçük değer `0` olabilir.
- **Pozitif doğal sayı / pozitif tam sayı** deniyorsa en küçük değer
  `1`'den başlar.

## Toplamı veya Çarpımı Sabit Sayı Çiftleri

- **Toplamı sabit** iki sayının **çarpımı**: sayılar birbirine
  **yaklaştıkça büyür**, birbirinden **uzaklaştıkça küçülür**.
  → En büyük çarpım için sayılar birbirine mümkün olduğunca **eşit/yakın**,
  en küçük çarpım için mümkün olduğunca **uzak** seçilir.
- **Çarpımı sabit** iki sayının **toplamı**: mantık ters işler — sayılar
  birbirine **yaklaştıkça toplam küçülür**, **uzaklaştıkça toplam büyür**.
  → En küçük toplam için çarpanlar birbirine mümkün olduğunca **yakın**
  seçilir.

## Doğrusal Denklemlerde Tam Sayı Çözümleri Bulma (`ax + by = c`)

- Denklemi cebirsel olarak çözmeye çalışmak yerine: bir değişkene küçük
  bir başlangıç değeri (genelde 0 veya 1) verilerek diğer değişkenin
  değeri bulunur.
- Sonraki çözümler, **x'in katsayısı kadar y'yi**, **y'nin katsayısı
  kadar x'i** ters yönlerde kaydırarak (biri artarken diğeri azalarak)
  bulunur — bu, tüm çözümleri tek tek denemeden sistematik biçimde
  üretmenin en hızlı yoludur.
- Hangi yönde (artarak mı azalarak mı) ilerleneceği, değişkenlerin sayı
  türüne (örn. doğal sayı olup olamayacağına) bağlıdır.

## Bölünebilme / Parçalama Teknikleri

- `(a + k·b)/b` biçimindeki ifadeler, bölme yoluyla **tam kısım +
  kesirli kısım** şeklinde ayrıştırılabilir (payda işlem boyunca
  değişmez). Kesirli kısmın **paydası**, o ifadenin tam sayı çıkması
  için **payı bölen bir sayı** olmalıdır.
- Tam sayılarla çalışılıyorsa, bir sayının **pozitif bölenlerinin
  yanı sıra negatif bölenleri** de dikkate alınmalıdır.
- Bir sayının bölenlerini bulurken **tam yarısına kadar** gidilir;
  yarısından sonra (kendisi hariç) başka bölen çıkmaz. Bu, özellikle
  büyük sayılarda zaman kazandırır.
- Bir değişkenin (`b` gibi) alabileceği bütün değerler tam sayı
  bölenlerse, bu değerlere karşılık gelen ifadenin (`a` gibi)
  **alabileceği değerler toplamı**, kısa yoldan şöyle bulunur:
  pozitif-negatif bölen çiftleri (`b` ve `-b`) ifadenin değişken kısmını
  birbirini götürecek şekilde sıfırlar; geriye yalnızca **sabit terim**
  kalır. Sonuç, bu sabit terimin **bölen sayısı kadar tekrarının
  toplamına**, yani `(sabit terim) × (bölen sayısı)` ifadesine eşittir.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

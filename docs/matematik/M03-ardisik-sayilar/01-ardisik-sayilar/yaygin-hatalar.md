# ⚠️ Yaygın Hatalar — ardışık sayılar

> Kaynak: Öğrencilerin sık yaptığı hatalar ve ÖSYM'nin kurduğu tuzaklar.
> Her madde; hata/tuzak örneği + derin kavrayışla çözümü şeklinde anlatılır.

## 1. Fark Verilen Sorularda Harfleri Tek Tek Açmak

**Hata:** `a, b, c` gibi ardışık sayılar arasındaki bir fark bilgisi
verildiğinde, her terim `x`, `x+2`, `x+4` gibi ayrı ayrı harflerle ifade
edilip uzun bir denklem sistemine dönüştürülür.

**Neden yanlış:** Ardışık sayıların farkı zaten **sabittir**; bu sabit
farkı doğrudan kullanmak yerine sıfırdan harflerle denklem kurmak, aynı
sonuca çok daha uzun bir yoldan ulaşmak demektir.

**Doğru çözüm:** Verilen fark bilgisini doğrudan, aranan farkın cinsinden
ifade ederek çöz; gereksiz harf tanımlamalarından kaçın.

## 2. Fark Sorusunda Harf Kullanmaya Devam Etmek

**Hata:** Soru yalnızca ardışık sayıların **farkıyla** ilgiliyken (sayı
değerleriyle değil), harflerle sembolik çözüme devam edilir.

**Neden yanlış:** Fark her zaman sabit olduğundan, harflerin yerine
dizinin türüne uygun küçük sayılar (`2, 4, 6` gibi) yazmak sonucu
değiştirmez ama işlemi çok kısaltır.

**Doğru çözüm:** Yalnızca fark soruluyorsa sayı kullan; sayıların
**kendisi** soruluyorsa (yani hangi spesifik sayılar olduğu isteniyorsa)
bu kısayol kullanılamaz, cebirsel ilişki kurulmalıdır.

## 3. Tek Terim Sayılı Toplamları Harflerle Çözmeye Çalışmak

**Hata:** "Ardışık 7 tek sayının toplamı 105" gibi bir soruda, sayılar
`x, x+2, x+4, x+6, x+8, x+10, x+12` şeklinde tek tek yazılıp toplanarak
`x` çözülmeye çalışılır.

**Neden yanlış:** Bu yöntem çok daha fazla işlem adımı gerektirir ve hata
riskini artırır.

**Doğru çözüm:** Toplamı terim sayısına böl, ortadaki sayıyı bul, oradan
istenen terime doğru ilerle.

## 4. Çift Terim Sayısında "Ortadaki Sayı"nın Diziye Ait Olduğunu Sanmak

**Hata:** Terim sayısı çift olduğunda (ör. 6 tane sayı), `Toplam / Terim
Sayısı` işleminden çıkan sayının doğrudan dizinin bir üyesi olduğu
varsayılır.

**Neden yanlış:** Terim sayısı çift olduğunda gerçek bir ortadaki terim
yoktur; bu işlemden çıkan sayı iki orta terimin **ortalamasıdır**
("aradaki sayı") ve dizinin gerçek bir üyesi olmayabilir.

**Doğru çözüm:** Çift terim sayısında çıkan sayıyı "aradaki sayı" olarak
yorumla; istenen terime bu aradaki sayıdan adım adım ilerleyerek ulaş.

## 5. Ardışık İki Sayının Toplamının Her Zaman Tek Olduğunu Unutmak

**Hata:** Bir sayının, ardışık iki sayının toplamı olarak yazılıp
yazılamayacağı sorgulanırken çift sayılar da aday olarak değerlendirilir.

**Neden yanlış:** Ardışık iki sayıdan biri her zaman tek, diğeri her
zaman çifttir; toplamları bu yüzden **her zaman tektir.** Çift bir sayı
hiçbir zaman ardışık iki sayının toplamı olamaz.

**Doğru çözüm:** Bu tip sorularda önce çift adayları hiç hesaba katmadan
ele; yalnızca tek sayılar için devam et.

## 6. Ardışık N Sayının Toplamının N'in Katı Olma Kuralını Yanlış Uygulamak

**Hata:** Ardışık terim sayısının **tek** olduğu durumlarda geçerli olan
"toplam, terim sayısının katıdır" kuralı, terim sayısı **çift** olan
gruplara da uygulanmaya çalışılır.

**Neden yanlış:** Bu kural yalnızca terim sayısı **tek** olduğunda kesin
olarak geçerlidir (çünkü o durumda ortadaki sayı bir tam sayıdır ve
toplam bu tam sayının terim-sayısı-katıdır). Terim sayısı çift olduğunda
böyle bir kesinlik yoktur.

**Doğru çözüm:** Kuralı yalnızca terim sayısı tek olan gruplara uygula;
çift terim sayılı gruplarda toplamı doğrudan terim sayısı × ortadaki
sayı ile hesapla, "N'in katı" kestirmesine güvenme.

## 7. Eksi Konan Terimin Etkisini Yalnızca 1 Katı Sanmak

**Hata:** Bir terimin önüne yanlışlıkla eksi konduğunda, doğru toplamla
yanlış toplam arasındaki farkın doğrudan o terime **eşit** olduğu
düşünülür.

**Neden yanlış:** Bir terimin önüne eksi koymak, o terimi hem
toplamamak hem de bir kez fazladan çıkarmak anlamına gelir — toplamdaki
azalma terimin **kendisinin 2 katı** kadardır, 1 katı değil.

**Doğru çözüm:** `Doğru Toplam − Yanlış Toplam` farkını bul, bu farkı
**2'ye böl**; çıkan sonuç aranan terimdir.

## 8. Çarpımsal Terimli Serilerde Tüm Terimleri Yeniden Hesaplamaya Çalışmak

**Hata:** `1×2 + 2×3 + ...` gibi bir seride yalnızca bir çarpan
değiştiğinde, tüm terimler yeniden tek tek çarpılıp yeni toplam eski
toplamdan çıkarılmaya çalışılır.

**Neden yanlış:** Bu yöntem gereksiz derecede uzundur ve hata riski
yüksektir; asıl değişimi taşıyan yalnızca değişen çarpanlardır.

**Doğru çözüm:** Değişmeyen çarpanları zihinsel olarak sil, geriye kalan
değişen çarpanların oluşturduğu yeni ardışık toplamı bul, bu toplamı
artış miktarıyla çarp.

[← Konu ana sayfasına dön](index.md) · [Hızlı Tekrar →](hizli-tekrar.md)

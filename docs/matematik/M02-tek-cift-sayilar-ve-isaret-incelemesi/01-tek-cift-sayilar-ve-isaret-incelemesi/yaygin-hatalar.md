# ⚠️ Yaygın Hatalar — Tek-Çift Sayılar ve İşaret İncelemesi

> Kaynak: Öğrencilerin sık yaptığı hatalar ve ÖSYM'nin kurduğu tuzaklar.
> Her madde; hata/tuzak örneği + derin kavrayışla çözümü şeklinde anlatılır.

## 1. Tek Katsayıyı Parite Belirleyici Sanmak

**Hata:** `3a` ifadesinde katsayı olan `3`'ün tek olmasından yola çıkarak
ifadenin tek/çift durumunun `3` tarafından belirlendiği sanılır (`3`
tekmiş, o zaman ifade de tektir gibi yanlış bir çıkarım yapılır).

**Neden yanlış:** Tek bir katsayı, çarpıldığı harfin tek/çift türünü
**değiştirmez.** `3a`'nın tek/çift olması tamamen `a`'ya bağlıdır: `a`
çiftse `3a` çift, `a` tekse `3a` tektir.

**Doğru çözüm:** Tek katsayıyı doğrudan sil, kalan harfi yorumla:
`3a` → `a` gibi düşün.

## 2. Kesirli (Tam Sayı Olmayan) Bir İfadeye Tek/Çift Etiketi Yapıştırmak

**Hata:** `1/2` ya da `1/3` gibi bir ifade için "tek midir çift midir"
sorusuna zorlama bir cevap üretilmeye çalışılır.

**Neden yanlış:** Bir sayının tek ya da çift olabilmesi için **öncelikle
tam sayı olması** gerekir. Tam sayı olmayan hiçbir ifade ne tektir ne
çifttir.

**Doğru çözüm:** `1/2` ve `1/3` gibi ifadeler için "ne tek ne çift" cevabı
verilir; bu, kuvvet negatif olduğunda ifadeyi kesire çeviren durumlarda
özellikle kritik hâle gelir (bkz. madde 3).

## 3. Kuvvetin Yalnızca "Tam Sayı" Olduğu Durumlarda Kesinlik Varmış Gibi Davranmak

**Hata:** `2^a` gibi bir ifade, `a` sadece tam sayı olarak verildiğinde
bile "2'nin katı olduğu için her zaman çifttir" diye yorumlanır.

**Neden yanlış:** Tam sayılar negatifleri de kapsar. `a` negatif olursa
(`2^-1 = 1/2` gibi) ifade **kesire dönüşür** ve tam sayı olmaktan çıkar
— dolayısıyla tek/çift sınıflandırması geçersiz kalır.

**Doğru çözüm:** Kuvvet yalnızca "tam sayı" olarak verilmişse, ifadenin
tek/çift olduğu **kesin olarak bilinemez**; bu tip öncüller doğrudan
elenir.

## 4. Doğal Sayı Kuvvette `0`'ın İstisnasını Atlamak

**Hata:** Çift tabanlı bir ifadenin kuvveti "doğal sayı" olarak
verildiğinde, ifadenin **her zaman** çift olduğu sanılır.

**Neden yanlış:** Doğal sayılar `0`'ı da kapsar ve herhangi bir sayının
`0`. kuvveti `1`'dir — `1` ise **tektir.** Bu durum, çift tabanlı
ifadenin "her zaman çift" olma kesinliğini bozar.

**Doğru çözüm:** Kuvvet doğal sayıysa çift tabanlı ifadelerde `0`
kuvvetini ayrıca kontrol et; genel kural sadece kuvvet `0`'dan farklıyken
geçerlidir.

## 5. İşaret Sorularında Çift Kuvvetli İfadeyi Yalnızca Kuvvetini Silerek Bırakmak

**Hata:** `a²` ifadesi işaret sorusunda `a`'ya indirgenir (yalnızca
kuvvet silinir), sanki tek kuvvetliymiş gibi işleme devam edilir.

**Neden yanlış:** Çift kuvvet daima **pozitif** sonuç verir ve çarpım/
bölümün işaretine **hiçbir katkı sağlamaz** (nötrdür). Bu yüzden yalnızca
kuvveti değil, **ifadenin tamamını** silmek gerekir.

**Doğru çözüm:** `a²` işaret sorusunda tamamen silinir; `a³` gibi tek
kuvvetli bir ifadede ise yalnızca kuvvet (`³`) silinir, `a` kalır.

## 6. Çıkarma İşleminde Büyük–Küçük Yönünü Karıştırmak

**Hata:** `x − y` işleminde sonucun işareti, hangi sayının büyük
olduğuna bakılmadan rastgele belirlenir.

**Neden yanlış:** Çıkarmada yön kritik önemdedir: **küçükten büyük**
çıkarılırsa sonuç **negatif**, **büyükten küçük** çıkarılırsa sonuç
**pozitif** olur.

**Doğru çözüm:** İşlemi yorumlamadan önce hangi sayının büyük olduğunu
belirle, sonucun işaretini ona göre ver.

[← Konu ana sayfasına dön](index.md) · [Hızlı Tekrar →](hizli-tekrar.md)

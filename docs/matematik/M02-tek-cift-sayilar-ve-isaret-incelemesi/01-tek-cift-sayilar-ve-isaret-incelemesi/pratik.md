# 💡 Pratik Bilgiler — Tek-Çift Sayılar ve İşaret İncelemesi

> Kaynak: Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## Çift Katsayı Kuralı

Bir ifadede harfin önünde **çift bir katsayı** varsa (`2a`, `4x` gibi),
o ifade **harfin ne olduğundan bağımsız olarak her zaman çifttir.**
Ancak bu, yalnızca o ifadenin kendisi için geçerlidir — harfin
(`a`, `x`) kendisi hakkında hiçbir şey söylemez; harf hâlâ tek de çift de
olabilir.

## Tek Katsayı Kuralı — "Tek Katsayıyı Sil Gitsin"

Bir ifadede harfin önünde **tek bir katsayı** varsa (`3a`, `5b` gibi),
bu katsayı ifadenin tek/çift olma durumunu **etkilemez** — sonucu
belirleyen tamamen harfin (`a`, `b`) kendi türüdür. Bu yüzden tek/çift
yorumu yaparken **tek katsayıyı doğrudan sil**, geriye kalan harfi
yorumla.

## Kuvvet Silme Kuralı (Tek/Çift Yorumunda)

- **Kuvvet pozitif tam sayıysa:** kuvveti komple sil, tabanı doğrudan
  yorumla (taban tekse sonuç tek, çiftse sonuç çift).
- **Kuvvet doğal sayıysa:** aynı kısayolu uygula ama **çift tabanlı**
  ifadelerde `0` kuvveti istisnasını unutma (`çift^0 = 1`, yani tektir).
- **Kuvvet yalnızca tam sayıysa (negatif olabilir):** bu kısayol
  **uygulanamaz**; ifadenin tek/çift olduğu kesin değildir, çünkü negatif
  kuvvet sonucu kesire çevirebilir.

## Kesinlik Yoksa Değer Ver

Soru kökünde **"kesinlikle"** ifadesi yoksa (yani soru "hangileri
kesinlikle tektir/çifttir" değil de sadece "hangileri tektir/çifttir"
diyorsa), harflerin yerine küçük, kullanışlı bir tek sayı (`1`) ve çift
sayı (`2`) yerleştirip doğrudan işlem yapılabilir. Kesinlik ifadesi
**varsa** bu kısayol kullanılamaz, klasik yoruma dönülür.

## Sayının Türünü Biliyorsan Doğrudan Değer Ver

Soru "M çift sayıdır" gibi bir sayının türünü doğrudan veriyorsa, o harfin
yerine en kolay çift değeri (`0` ya da `2`) veya tek değeri (`1`) yazıp
ifadeleri doğrudan hesaplamak, uzun yorum yapmaktan çok daha hızlıdır.

## İşaret Sorularında Kuvvet Silme Kısayolu

- **Tek kuvvetli ifade:** yalnızca kuvveti sil, tabanın işaretini olduğu
  gibi bırak (tek kuvvet işareti değiştirmez).
- **Çift kuvvetli ifade:** ifadenin **tamamını** sil — çünkü çift kuvvet
  daima pozitif sonuç verir ve bu, çarpım/bölümün işaretine hiçbir katkı
  sağlamaz (nötrdür).

## Çıkarmayı Toplama Gibi Yorumlama

`a − b` ifadesinin tek/çift durumunu yorumlarken, bunu `a + b` gibi
düşünebilirsin — toplama ve çıkarma, tek/çift sonucu açısından birbirinin
birebir eşdeğeridir. Bu, iki harfli ifadelerde yorumu hızlandırır.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

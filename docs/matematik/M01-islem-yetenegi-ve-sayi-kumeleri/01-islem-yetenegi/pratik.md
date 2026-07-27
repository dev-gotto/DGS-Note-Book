# 💡 Pratik Bilgiler — İşlem Yeteneği

> Kaynak: Hocanın anlatımına dayalı uygulama yöntemleri ve kısayollar.

## En Büyük / En Küçük Değer Verirken Katsayı Mantığı

Bir ifadenin en büyük ya da en küçük değerini bulman istendiğinde önce
**hangi harfin katsayısı büyük** ona karar ver:

- İfadeyi **büyütmek** istiyorsan, katsayısı büyük olan harfe **daha
  büyük** değer ver.
- İfadeyi **küçültmek** istiyorsan, katsayısı büyük olan harfe yine
  **daha küçük** değer ver (çıkarma işlemindeki harf için mantık ters
  işler — bkz. Sayı Kümeleri alt-konusu, Örnek 1).

## Oran İfadelerinde Harflendirme (K Kısayolu)

`a/b` şeklinde bir oran verilmişse, kesri parçalara ayırmak yerine ortak
bir `k` değişkeni ata:

- `a/b = 2/3` verilmişse → `a = 2k`, `b = 3k`
- `a/2 = b/3` gibi ters verilmişse → yine `a = 2k`, `b = 3k` (altındaki
  sayıların katları olur)
- `2a = 3b` gibi bir eşitlik verilmişse → harflere **ters** değerler
  verilir: `a = 3k`, `b = 2k` (üç format da aslında aynı oranı, `a/b = 3/2`
  ilişkisini, ifade eder)

Sadeleştirme yapmak (`6a = 15b` → `2a = 5b`) `k` ile çalışmayı
kolaylaştırır ama zorunlu değildir; sadeleştirmeden de aynı sonuca
ulaşılır.

## Kutu / Sembol Sorularında "Elini Korkak Alıştırma"

Kutu ya da sembol içine sayı/işlem yerleştirme sorularında uzun uzun
düşünmek yerine **direkt denemeye başla**: bir işlemi (artı mı, eksi mi,
çarpı mı) doğrudan dene, tutmuyorsa bir sonrakine geç. Bu sorular zaten
deneme-yanılma ile çözülecek şekilde kurgulanır; detaylı strateji için
bkz. [🎯 Soru Çözüm Stratejileri](strateji.md).

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

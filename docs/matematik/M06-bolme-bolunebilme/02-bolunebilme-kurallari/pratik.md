# 💡 Pratik Bilgiler — bölünebilme kuralları

## 3 ve 9 Kuralında "Atma" Taktiği

Rakamları tek tek toplayıp sonra bölmek yerine: rakamlar arasında **3'ün katı** (3 kuralı için) ya da **9'un katı** (9 kuralı için) olan rakam grupları görüldükçe direkt **atılır** (yok sayılır). Geriye kalan rakamlar toplanır, gerekirse o da 3'e/9'a bölünür.

**Örnek mantık (3 kuralı):** Rakamlar 3, 7, 4, 2, 5, 9, 8 olsun. 3 zaten 3'ün katı → at. 7 ile 4 → 7+4=11, katı değil, tut. 2 ile 5 ile 9 → 2+5=7, +9=16, katı değil ama 9'un kendisi zaten 3'ün katı, sadece 9'u at, 2 ve 5 kalsın. Sonunda geriye kalan küçük rakamlar toplanıp 3'e bölünür. Bu taktik büyük sayılarla rakam toplama işini kısaltır.

## 8 ve 9'un Kuvvet Mantığıyla Genellenmesi

2'nin kuvvetleri (2, 4, 8, 16, 32, ...) için "sondan kaç basamağa bakılır" sorusu, üssü bularak cevaplanır: $2^n$ ile bölünebilmek için sondan **n** basamağa bakılır (2→1, 4→2, 8→3, 16→4, 32→5, ...). DGS'de doğrudan "16 ile bölünebilme kuralı" sorulmaz ama "bir sayının 32 ile bölümünden kalanı bulmak için sondan en az kaç basamağa bakılır" tarzı yorum soruları bu genellemeyle çözülür.

## 11 ile Bölme: Bölüm Kısayolu (İleri Seviye)

3 basamaklı $\overline{abc}$ sayısı 11'e tam bölünüyorsa, bölümü (sonucu) bulmak için:

- $a+c$ toplamı doğrudan $b$'yi **veriyorsa**: ortadaki rakam ($b$) silinir, kalan iki rakam ($a$ ve $c$) yan yana yazılarak bölüm elde edilir.
- $a+c-b$ işlemi **11 veriyorsa**: yine ortadaki rakam silinir, ama bu kez $a$ rakamı **1 azaltılarak** yazılır (yani "onlar basamağından 1 ödünç alınmış" gibi düşünülür).

**Örnek:** 495 → 4+5=9, ortadaki 9'u veriyor → sil, kalan 45 → 495 = 45×11.
**Örnek:** 209 → 2+9=11, ortadaki 0'ı vermiyor ama $2+9-0=11$ → sil, baştaki rakamı 1 azalt (2→1) → kalan 19 → 209 = 19×11.

## Kuralı Olmayan Sayılarla Bölünebilme (Çarpanlara Ayırma Yöntemi)

2, 3, 4, 5, 8, 9, 10, 11 dışındaki sayıların (6, 12, 14, 15, 18, 20, 22, 24, 30, 33, 36, 40, 44, 45, 55, 60, 66, 72, 88, 90, 99, ... gibi) kendine ait bir bölünebilme kuralı **yoktur**. Bu sayılarla bölünebilme şöyle test edilir:

1. Sayı, **aralarında asal** (ortak böleni 1'den başka olmayan) iki çarpana ayrılır.
2. Bu iki çarpanın **her ikisinin de kendine ait bir bölünebilme kuralı** (yukarıdaki 2/3/4/5/8/9/10/11 listesinden) olması gerekir.
3. Verilen sayı, her iki çarpana da **ayrı ayrı** tam bölünüyorsa, orijinal sayıya da tam bölünür.

**Neden aralarında asal olmalı?** Çarpanların ortak böleni varsa (ör. 12'yi 2×6 olarak ayırmak), aynı bölünebilirlik bilgisi (ör. çiftlik) iki çarpanda da tekrarlanmış olur ve sonuç yanıltıcı çıkabilir; bu yüzden mutlaka ortak böleni olmayan bir çift seçilir (ör. 12 = 3×4, 2×6 değil).

### Sık Kullanılan Ayrımlar

| Sayı | Aralarında Asal Çarpanlar | Kontrol Sırası |
|---|---|---|
| 6 | 2 × 3 | önce 2, sonra 3 |
| 12 | 4 × 3 | önce 4, sonra 3 |
| 15 | 5 × 3 | önce 5, sonra 3 |
| 18 | 2 × 9 | önce 2, sonra 9 |
| 20 | 5 × 4 | önce 4, sonra 5 |
| 22 | 2 × 11 | önce 2, sonra 11 |
| 24 | 8 × 3 | önce 8, sonra 3 |
| 30 | 10 × 3 | önce 10, sonra 3 |
| 33 | 3 × 11 | önce 3, sonra 11 |
| 36 | 4 × 9 | önce 4, sonra 9 |
| 40 | 8 × 5 | önce 8, sonra 5 |
| 44 | 4 × 11 | önce 4, sonra 11 |
| 45 | 5 × 9 | önce 5, sonra 9 |
| 55 | 5 × 11 | önce 5, sonra 11 |
| 72 | 8 × 9 | önce 8, sonra 9 |
| 88 | 8 × 11 | önce 8, sonra 11 |
| 90 | 10 × 9 | önce 10, sonra 9 |
| 99 | 9 × 11 | önce 9, sonra 11 |

### Kontrol Sırası Kuralı

Rakamları **toplayarak** kontrol edilen kurallar (3, 9, 11) her zaman **en sona** bırakılır; basamak bakarak (son 1/2/3 basamak) kontrol edilen kurallar (2, 4, 5, 8, 10) önce uygulanır. Sebep: basamak-bazlı kurallar bilinmeyenin değerini doğrudan **daraltır** (az sayıda ihtimale indirger); rakam toplama kuralları bu daralan ihtimaller üzerinde daha hızlı elenir.

## Kalanlı Sorularda Kuralsız Sayı Yöntemi

Bir sayı $n$'ye (kuralsız, ör. 30'a) bölündüğünde kalan $k$ verilmişse: $n = p \times q$ (aralarında asal iki çarpana ayrılmış) olduğunda, **aynı $k$ kalanı**, sayının hem $p$'ye hem de $q$'ya bölümünde de geçerlidir. Yani sayının 30'a bölümünden kalanı 1 ise, aynı sayının 10'a bölümünden kalanı da 1'dir, 3'e bölümünden kalanı da 1'dir — bu iki bilgi ayrı ayrı kullanılarak bilinmeyenler bulunur.

## "Bir Şey Olmuşsa Olmuştur" Yaklaşımı

Soru "... olabilir mi", "kaçtır" gibi **tek bir kesin cevap** arıyorsa (en az/en çok değil), akla gelen ilk uygun deneme koşulları sağlıyorsa o an cevaba ulaşılmış demektir; başka ihtimalleri de sağlayıp sağlamadığını tek tek doğrulamaya gerek yoktur. Bu yaklaşım özellikle çok koşullu ("hem şuna hem buna bölünsün") sorularda zaman kazandırır.

## "Geometrik Sayı" Tipi Uydurma Tanım Soruları

DGS'de bazen gerçek bir matematik terimi olmayan, sorunun kendi içinde tanımladığı kavramlar (ör. "bir çokgenin kenar sayısına tam bölünen sayıya geometrik sayı denir") verilir. Bu tip sorular yeni bir kural gerektirmez; verilen tanım okunup mevcut bölünebilme kurallarına (2, 3, 4, 5, 8, 9, 10, 11 ya da bunların kuralsız kombinasyonlarına) indirgenir.

[← Konu ana sayfasına dön](index.md) · [Soru Bankası →](soru-bankasi.md)

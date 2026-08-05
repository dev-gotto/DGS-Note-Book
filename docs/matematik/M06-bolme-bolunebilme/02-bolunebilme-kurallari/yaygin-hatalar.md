# ⚠️ Yaygın Hatalar — bölünebilme kuralları

> Kaynak: Öğrencilerin sık yaptığı hatalar ve ÖSYM'nin kurduğu tuzaklar.
> Her madde; hata/tuzak örneği + derin kavrayışla çözümü şeklinde anlatılır.

## 1. Kontrol Sırasını Rastgele Seçmek

**Hata:** Bir sayı birden fazla kurala aynı anda uyduğunda (ör. 15,
36, 45 gibi çoklu koşullu sorularda), rakam toplama kuralına (3, 9,
11) basamak kuralından (2, 4, 5, 8, 10) önce bakılır; bu da işlemi
gereksiz yere uzatır ve bazen fazladan ihtimal üretir.

**Neden yanlış:** Basamak bazlı kurallar bilinmeyeni doğrudan dar bir
kümeye (çoğu zaman tek bir değere) indirger; bu daraltma yapılmadan
rakam toplama kuralına geçmek, gereksiz yere geniş bir aralık üzerinde
çalışmaya yol açar.

**Doğru çözüm:** Her zaman önce basamağa bakılan kural (2, 4, 5, 8, 10),
sonra rakam toplamına bakılan kural (3, 9, 11) uygulanır (bkz. Örnek 4,
Örnek 9, Örnek 12).

## 2. Kuralı Olmayan Sayıyı Ortak Bölenli Çarpanlara Ayırmak

**Hata:** 12 gibi kuralı olmayan bir sayı, aralarında asal olmayan
çarpanlara (ör. 12 = 2 × 6) ayrılır; bu durumda bölünebilirlik testi
yanlış veya eksik sonuç verir.

**Neden yanlış:** Çarpanların ortak böleni varsa (2 ve 6'nın ortak
böleni 2'dir), aynı bölünebilirlik bilgisi (çiftlik) her iki çarpanda
da tekrarlanmış olur; bu sayının gerçekten 12'ye bölünüp
bölünmediğini garanti etmez.

**Doğru çözüm:** Kuralı olmayan bir sayı her zaman **aralarında asal**
ve her ikisinin de kendine ait kuralı olan iki çarpana ayrılır (ör. 12
= 3 × 4, 2 × 6 değil); bkz. pratik.md — Sık Kullanılan Ayrımlar
tablosu.

## 3. 5'e Bölümden Kalan Sorularında Tek İhtimal Sanmak

**Hata:** "Sayının 5'e bölümünden kalanı 2'dir" bilgisinden, sayının
son rakamının **yalnızca 2** olabileceği sonucu çıkarılır; 5 eklenmiş
diğer ihtimal (7) gözden kaçırılır.

**Neden yanlış:** 5 kuralında (10 kuralından farklı olarak) bir kalan
değeri için **iki** olası son rakam vardır: $k$ ve $k+5$ (ör. kalan 2
ise son rakam 2 ya da 7 olabilir). Bu ikinci ihtimal atlanırsa
toplam/sayım sorularında eksik cevap çıkar.

**Doğru çözüm:** "5'e bölümünden kalan $k$" bilgisi görüldüğünde her
zaman iki aday ($k$ ve $k+5$) birlikte değerlendirilir (bkz. Örnek 12).

## 4. 11 Kuralında Yanlış Taraftan veya Yanlış İşaretle Başlamak

**Hata:** Alternatif toplam-fark işlemi soldan başlatılır ya da en
sağdaki rakama eksi işareti verilir.

**Neden yanlış:** 11 kuralının ispatı, 10'un kuvvetlerinin (birler,
onlar, yüzler, ...) 11'e göre sırasıyla $+1, -1, +1, -1, \dots$
fazlalık verdiği gerçeğine dayanır; bu sıra **birler basamağından**
(en sağdan) başlar ve ilk işaret her zaman **artı**dır. Yanlış
taraftan başlamak tamamen farklı (ve yanlış) bir sonuç üretir.

**Doğru çözüm:** 11 kuralı uygulanırken mutlaka en sağdaki rakamdan
başlanır, ona artı işareti verilir, sonra sırayla eksi-artı-eksi
devam edilir (bkz. Örnek 5, Örnek 13).

## 5. 11 Kuralında Sonucu 0–11 Aralığına İndirmeyi Unutmak

**Hata:** Alternatif toplam işleminin sonucu $11$'den büyük ya da
negatif çıktığında, bu değer sorgulanmadan doğrudan kalan olarak kabul
edilir.

**Neden yanlış:** Kalan tanım gereği $0$ ile bölenden (burada $11$'den)
küçük bir doğal sayı olmalıdır. Sonuç $11$'den büyükse içinden $11$
çıkarılmalı (gerekirse tekrar tekrar), negatifse üzerine $11$
eklenmelidir; aksi hâlde bulunan "kalan" matematiksel olarak
geçersizdir.

**Doğru çözüm:** 11 kuralının sonucu her zaman $0$–$11$ aralığına
indirilene kadar düzeltilir; sonuç $0$ çıkarsa sayı zaten $11$'e tam
bölünür (bkz. Örnek 5).

## 6. Kalanlı Kuralsız Sayı Sorularında Kalanı Yalnızca Bir Çarpana Uygulamak

**Hata:** "$X$'in $30$'a bölümünden kalanı $1$'dir" gibi bir bilgi
verildiğinde, bu kalan yalnızca çarpanlardan birine (ör. sadece
$10$'a) uygulanır; diğer çarpana ($3$'e) aynı kalanın geçerli olduğu
unutulur.

**Neden yanlış:** $30 = 3 \times 10$ (aralarında asal) olduğunda,
$30$'a bölümünden kalan $k$ ise, **aynı $k$ kalanı** hem $3$'e hem
$10$'a bölümde de geçerlidir; bu bilgi atlanırsa denklemin yarısı
kullanılmamış olur ve bilinmeyen tam olarak bulunamaz.

**Doğru çözüm:** Kuralsız bir sayıya bölümden kalan verildiğinde, bu
kalan çarpanlara ayrıldıktan sonra **her iki çarpana da ayrı ayrı**
uygulanır (bkz. Örnek 11).

## 7. "Rakamları Farklı" Gibi Ek Kısıtları Unutup Tüm Adayları Cevaba Katmak

**Hata:** Bölünebilme kurallarından bir aday kümesi (ör. $A \in
\{1,4,7\}$) bulunduktan sonra, soruda geçen "rakamları farklıdır" gibi
bir ek kısıt kontrol edilmeden tüm aday değerler toplama/cevaba dahil
edilir.

**Neden yanlış:** Bir aday, sayıda zaten kullanılmış başka bir rakamla
çakışıyorsa (ör. $A=1$ iken $B$ zaten $1$ ise), bu aday geçersizdir;
kontrol edilmezse fazladan (yanlış) bir değer toplama girer.

**Doğru çözüm:** Bölünebilme kurallarından gelen her aday, cevaba
eklenmeden önce sorudaki tüm ek kısıtlarla (özellikle "rakamları
farklıdır") tek tek karşılaştırılır (bkz. Örnek 10, Örnek 12).

## 8. "Biri Yanlış" Türü Sorularda Rastgele Deneme Yapmak

**Hata:** Birden fazla bölünebilme bilgisi verilip yalnızca birinin
yanlış olduğu söylendiğinde, hangi bilginin yanlış olduğu sistematik
bir mantık kurulmadan tahmin edilir.

**Neden yanlış:** Bu tip sorularda bilgiler arasında çoğu zaman bir
**içerme ilişkisi** vardır (ör. $10$'a bölünmek $2$'ye ve $5$'e
bölünmeyi de zorunlu kılar, $9$'a bölünmek $3$'e bölünmeyi zorunlu
kılar); bu ilişki kurulmadan yapılan rastgele deneme, birden fazla
bilginin aynı anda çökmesine (ve "yalnızca bir yanlış" koşuluyla
çelişmeye) yol açabilir.

**Doğru çözüm:** Önce hangi bilgilerin "yanlış olması hâlinde başka
bilgileri de yanlış yapacağı" belirlenir; bu tür bilgiler kesin
**doğru** kabul edilir. Yanlış olan bilgi, geriye kalan (başka bir
bilgiyi zorunlu kılan ama kendisi zorunlu kılınmayan) taraftan çıkar
(bkz. Örnek 6).

[← Konu ana sayfasına dön](index.md) · [Hızlı Tekrar →](hizli-tekrar.md)

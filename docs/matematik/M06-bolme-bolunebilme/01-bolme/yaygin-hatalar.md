# ⚠️ Yaygın Hatalar — bölme

> Kaynak: Öğrencilerin sık yaptığı hatalar ve ÖSYM'nin kurduğu tuzaklar.
> Her madde; hata/tuzak örneği + derin kavrayışla çözümü şeklinde anlatılır.

## 1. Bölen>Kalan Kuralını Hiç Aramamak

**Hata:** Harfli bir bölme sorusunda bilinmeyeni bulmak için tek bilgi
kaynağı olarak bölmenin sağlaması (${A=B\times C+K}$) kullanılır;
bilinmeyeni izole etmek için ikinci bir bilgiye ihtiyaç duyulduğunda
nereye bakılacağı bilinmez.

**Neden yanlış:** Bölme sorularının neredeyse tamamı yalnızca iki
bilgiyle çözülür: sağlama formülü ve **bölen kalandan büyüktür**
kuralı. Bu ikinci kural akla gelmeyince soru "eksik bilgili" gibi
görünür, oysa eksik olan bilgi bu kuraldan gelir.

**Doğru çözüm:** Bir bölme sorusunda bilinmeyen bulunamıyorsa ilk
refleks bölen>kalan eşitsizliğini yazmak olmalı; bu, bilinmeyen için
bir aralık (dolayısıyla "en büyük/en küçük" ya da tek bir kesin değer)
verir (bkz. Örnek 1, Örnek 2).

## 2. Kalanın Negatif ya da Bölenden Büyük Çıkmasına İzin Vermek

**Hata:** Bir çözümde kalan olarak eksi bir sayı ya da bölenden büyük/
eşit bir sayı bulunur ve bu sonuç sorgulanmadan kabul edilir.

**Neden yanlış:** Kalan tanım gereği her zaman bir doğal sayıdır
($K \geq 0$) ve bölenden **kesinlikle küçüktür** ($B>K$). Eksi ya da
bölenden büyük bir kalan çıkması, işlemin bir yerinde hata yapıldığının
kesin göstergesidir.

**Doğru çözüm:** Bir çözümün sonunda kalan negatif veya bölene eşit/
büyük çıkarsa, sonuç asla olduğu gibi bırakılmaz; işlem gözden geçirilir
(gerekiyorsa bölüm bir azaltılıp kalan tekrar hesaplanır).

## 3. İki Bölme Denklemini Doğrudan Birbirinin Yerine Koymaya Çalışmak

**Hata:** İki ayrı bölme denklemi, istenen ifadeyi (ör. "$B$'nin $A,C$
türünden eşiti") doğrudan içermiyorsa, bir denklemdeki terim diğerinin
içine zorla yerleştirilmeye çalışılır; bu genelde bir çıkmaz sokağa
girmeye ve soruyu terk etmeye yol açar.

**Neden yanlış:** İki denklem farklı bilinmeyenler içeriyorsa (ör.
birinde $a$ yok, diğerinde $c$ yok), doğrudan yerine koyma çoğu zaman
mümkün değildir; bu bir "yerine koyma sorusu" değil bir **taraf tarafa
işlem sorusu**dur.

**Doğru çözüm:** İki bölme denklemi, aranan ifadeyi ancak toplanır ya
da çıkarılırsa ortaya çıkarıyorsa taraf tarafa toplama/çıkarma
denenmelidir; terimlerin birbirini götürüp aranan harfi yalnız
bırakması beklenir (bkz. Örnek 3).

## 4. Çarpımdaki Hangi İfadenin "Bölen" Olduğunu Yanlış Belirlemek

**Hata:** Bir bölme sağlamasında birden fazla çarpan/terim varken
(ör. $5 \times (B+4)$), bölen>kalan kuralı uygulanırken çarpımın
tamamı ya da yanlış parçası "bölen" sanılır.

**Neden yanlış:** Bölen>kalan kuralı yalnızca gerçek **bölene**
(sağlama formülündeki $B$'ye, yani sabit çarpana veya çarpımdaki doğru
faktöre) uygulanır; çarpımın diğer parçası (bölüm) bu kurala girmez.

**Doğru çözüm:** Bölen>kalan kuralını yazmadan önce sağlama
formülündeki $A=B\times C+K$ eşleşmesini net biçimde çıkar: hangi
ifade $B$ (bölen), hangisi $C$ (bölüm), hangisi $K$ (kalan) — kural
yalnızca $B$ ile $K$ arasında kurulur (bkz. Örnek 2'de birinci
bölmenin bölen $b-1$'dir, ikinci bölmenin bölen $5$'tir; ikisi
karıştırılmamalıdır).

## 5. Kalan Bulma Sorularında Sayının Tam Açılımını Şıklara Yazmak

**Hata:** "$a$'nın $n$'e bölümünden kalanı $k$'dır" bilgisi verildiğinde,
$a$ yerine $nq+k$ (harfli, genel) ifadesi yazılıp bu ifade şıklardaki
karmaşık işlemlere (kare, küp, çarpım vb.) uygulanmaya çalışılır.

**Neden yanlış:** Bu yaklaşım matematiksel olarak doğru olsa da işlemi
gereksiz yere devasa büyütür; harfli bir ifadenin küpünü almak gibi bir
işlem pratikte yapılabilir/çözülebilir değildir.

**Doğru çözüm:** Kalan bulma işlemlerinde sayının yerine **doğrudan
kalanı** koy; $a$'nın yerine harfli ifadesini değil, verilen $k$
değerini yaz (bkz. Örnek 6, Örnek 7).

## 6. Sayı Atarken Büyük veya Elverişsiz Bir Değer Seçmek

**Hata:** Harften sayıya geçiş (sayı atama) tekniği kullanılırken
bölen>kalan koşuluna uyan ama gereksiz büyük/karmaşık bir sayı
seçilir; işlem uzar ve hata riski artar.

**Neden yanlış:** Tekniğin amacı işlemi **basitleştirmektir**; büyük
bir sayı seçmek bu amacı boşa çıkarır ve harfli çözümden daha yavaş
sonuca ulaşılmasına yol açar.

**Doğru çözüm:** Doğal sayı kısıtı varsa mümkün olan en küçük değeri
(genelde $0$ veya $1$) seç; koşulu sağlayan en küçük/en basit sayı her
zaman en hızlı yoldur (bkz. Örnek 4).

## 7. Görünüşte "Boşa Verilmiş" Bir Bilgiyi Kullanmayı Atlamak

**Hata:** Bölen>kalan kuralından geniş bir aralık (birden fazla aday
değer) elde edildiğinde, soruda geçen ama henüz kullanılmamış bir sayı/
rakam (ör. bir sayının belirli bir basamağı) göz ardı edilir ve
aralıktaki **tüm** değerler cevaba dahil edilir.

**Neden yanlış:** ÖSYM tarzı sorular boşuna bilgi vermez; kullanılmamış
görünen her sayı/rakam genelde bir ek daraltma koşuludur (en sık
görüleni: teklik-çiftlik). Bu koşul atlanırsa toplam/sayım sorularında
fazladan (yanlış) değerler cevaba dahil edilir.

**Doğru çözüm:** Bölen>kalan aralığını bulduktan sonra soruda henüz
kullanılmamış her veriyi tekrar kontrol et; özellikle son basamağı
belirtilen bir sayı görürsen mutlaka teklik-çiftlik açısından incele
(bkz. Örnek 10).

## 8. Periyodik Kalan Sorularında Toplamı Doğrudan Yeni Bölene Bölmenin Yeterli Olduğunu Sanmak

**Hata:** "$K$'nın kalanı $k_1$, $L$'nin kalanı $k_2$ ise $K+L$'nin
yeni bir bölene göre kalanı $(k_1+k_2)$'nin o bölene bölümünden
kalandır" denip işlem burada bitirilir; $K+L$'nin aslında **birden
fazla** değer alabileceği ve bu değerlerin farklı kalanlar
üretebileceği gözden kaçırılır.

**Neden yanlış:** $K$ ve $L$'nin kalanları aynı bölene (ör. $4$) göre
verilmişse, $K+L$ de bu bölenin katları kadar aralıklarla artan sonsuz
bir değer kümesidir; soru **yeni bir bölene** (ör. $8$) göre kalan
sorduğunda, bu farklı $K+L$ değerleri farklı kalanlar üretebilir.

**Doğru çözüm:** Soru "farklı kalanların toplamı"nı istiyorsa,
$K+L$'nin alabileceği birkaç ardışık değeri (aynı periyotla artan)
tek tek yeni bölene böl, kalanların tekrar etmeye başladığı noktayı
gör, yalnızca **farklı** kalanları topla (bkz. Örnek 11).

[← Konu ana sayfasına dön](index.md) · [Hızlı Tekrar →](hizli-tekrar.md)

# 📘 Teorik Bilgiler — bölme

## Bölmenin Elemanları

Bir **A** doğal sayısı, **B** doğal sayısına bölündüğünde bir **bölüm** ve bir **kalan** elde edilir:

| Sembol | Adı |
|---|---|
| A | Bölünen |
| B | Bölen |
| C | Bölüm |
| K | Kalan |

## Bölmenin Sağlaması (Temel Özdeşlik)

Bölme işleminin doğruluğu her zaman şu eşitlikle kontrol edilir:

$$A = B \times C + K$$

Bu özdeşlik, DGS'de bölme ve bölünebilme ile ilgili neredeyse tüm soruların çözüm iskeletini oluşturur. Bilinmeyen bir eleman (genellikle bölünen), diğer üç elemanın yerine yazılıp bu formülle bulunur.

## Kalanla İlgili İki Zorunlu Kural

1. **Bölen, kalandan büyüktür:** $B > K$. Bu, bölme işleminin tanımı gereği zorunludur — kalan bölene eşit ya da ondan büyük olsaydı, bölme işlemi bitmemiş sayılırdı.
2. **Kalan, negatif olamaz:** Kalan her zaman bir doğal sayıdır, yani $K \geq 0$. Kalan asla eksi bir değer olarak bulunamaz; bir çözümde eksi kalan çıkıyorsa yapılan işlemde hata var demektir.

Bu iki kural (sağlama formülü + $B>K$ eşitsizliği), harfli/bilinmeyenli bölme sorularının tamamını çözmeye yeter; başka bir "numara" gerekmez.

## Tam Bölünebilme

Kalan $K=0$ olduğunda, A sayısı B'ye **tam bölünür** denir. Bu durumda:

$$A = B \times C$$

A, hem B'nin hem de C'nin tam katıdır; yani A, B'ye de C'ye de tam bölünür.

## Kalan Bulma İlkesi (Sayının Yerine Kalanını Kullanma)

Bir A sayısının B'ye bölümünden kalan K ise, A sayısı toplama, çıkarma ve çarpma işlemlerinde **doğrudan K ile değiştirilebilir** — sonucun B'ye bölümünden elde edilecek kalan değişmez. Yani:

- Eğer $a$'nın B'ye bölümünden kalanı $k_1$, $b$'nin B'ye bölümünden kalanı $k_2$ ise:
    - $(a+b)$'nin B'ye bölümünden kalanı, $(k_1+k_2)$'nin B'ye bölümünden kalanına eşittir.
    - $(a-b)$'nin B'ye bölümünden kalanı, $(k_1-k_2)$'nin B'ye bölümünden kalanına eşittir (negatif çıkarsa B eklenerek doğal sayıya çevrilir).
    - $(a \times b)$'nin B'ye bölümünden kalanı, $(k_1 \times k_2)$'nin B'ye bölümünden kalanına eşittir.

Bu ilkenin arkasındaki sebep: aynı sayıya bölündüğünde **aynı kalanı veren sayılar** (ör. 5'e bölündüğünde kalanı 2 olan 2, 7, 12, 17, 22, ...) toplama/çıkarma/çarpma işlemlerinde birbirinin yerine kullanılabilir, çünkü her biri $B \times (\text{tam sayı}) + K$ biçiminde yazılabilir ve $B$'nin katı olan kısım işlemin kalanını etkilemez.

## Bir Toplamın/Kalan Zincirinin Farklı Bölenle Yeniden Bölünmesi

Kalan bulma işleminde önce sayının yerine kalanı konur, bulunan yeni ifade orijinal bölene göre işlenir; eğer bu işlemin sonucu bölenden büyük çıkarsa, sonuç tekrar aynı bölene bölünüp nihai (bölenden küçük) kalan elde edilir. Kalan hiçbir aşamada negatif ya da bölenden büyük/eşit bırakılmaz.

[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)

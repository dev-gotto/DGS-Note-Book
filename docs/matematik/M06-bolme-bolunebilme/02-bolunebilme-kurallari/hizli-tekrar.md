# Hızlı Tekrar — bölünebilme kuralları

- **Kendine ait kuralı olan sayılar:** yalnızca $2, 3, 4, 5, 8, 9, 10,
  11$. Bunların dışında (6, 7, 12, ...) hiçbir sayının kendine özgü
  kuralı yoktur.
- **2:** birler basamağı çift ($0,2,4,6,8$) → tam bölünür; tekse kalan
  $1$.
- **3:** rakamları toplamı $3$'ün katı → tam bölünür; değilse kalan,
  rakamlar toplamının $3$'e bölümünden kalana eşit. ("3'ün katı olan
  rakamları at" taktiği işlemi kısaltır.)
- **4:** son iki basamak $4$'ün katı → tam bölünür; değilse kalan,
  yalnızca son iki basamağın $4$'e bölümünden gelir.
- **5:** son rakam $0$ ya da $5$ → tam bölünür; kalan $k$ ise son
  rakam $k$ ya da $k+5$ olabilir (iki ihtimal!).
- **8:** son üç basamak $8$'in katı → tam bölünür; değilse kalan,
  yalnızca son üç basamağın $8$'e bölümünden gelir.
- **9:** rakamları toplamı $9$'un katı → tam bölünür (3 ile aynı
  mantık, "9'un katı olan rakamları at" taktiği).
- **10:** son rakam $0$ → tam bölünür; değilse kalan doğrudan **son
  rakamın kendisi** (tek ihtimal, 5 kuralından farklı).
- **11:** sağdan başlayarak $+,-,+,-,\dots$ işaretiyle rakamları
  topla/çıkar; sonuç $0$ ise tam bölünür, $0$–$11$ dışına çıkarsa $11$
  eklenip/çıkarılarak bu aralığa indirilir. 3 basamaklı sayılarda:
  baştaki + sondaki = ortadaki ise tam bölünür.
- **11'e bölmenin bölüm kısayolu (3 basamaklı):** baştaki+sondaki
  ortadakini veriyorsa ortadaki silinir, kalan iki rakam bölümdür;
  vermiyor ama baştaki+sondaki−ortadaki $=11$ ediyorsa yine ortadaki
  silinir, baştaki rakam $1$ azaltılarak yazılır.
- **Kuralların ispat mantığı:** 2/4/8 → $2^1, 2^2, 2^3$ oldukları için
  sondan 1/2/3 basamağa bakılır (genelleme: $2^n$ için sondan $n$
  basamak). 3/9 ve 11 → basamak değerleri ($100a+10b+c$ gibi)
  $9$'un/$11$'in katı + rakamın kendisi biçiminde ayrıştırılabildiği
  için rakamları toplama/alternatif toplama kuralı ortaya çıkar.
- **Kontrol sırası kuralı:** basamak bazlı kurallar (2,4,5,8,10) her
  zaman önce, rakam toplama kuralları (3,9,11) her zaman en son
  uygulanır — basamak kuralları bilinmeyeni daha hızlı daraltır.
- **Kuralı olmayan sayı (6, 12, 15, 30, 36, 45, 88, 99, ...):**
  aralarında asal (ortak böleni olmayan) ve her ikisinin de kendine
  ait kuralı olan iki çarpana ayrılır; sayı her iki çarpana da ayrı
  ayrı tam bölünüyorsa orijinal sayıya da bölünür.
- **Kalanlı kuralsız sayı sorusu:** bir sayının kuralsız bölene (ör.
  30) göre kalanı $k$ ise, bu $k$ kalanı, o bölenin aralarında asal
  çarpanlarının **her ikisine göre de** aynen geçerlidir.
- **"Bir şey olmuşsa olmuştur":** "kaçtır" tipi (en az/en çok değil)
  sorularda koşulları sağlayan ilk uygun deneme bulununca iş biter,
  başka ihtimal aranmaz.
- **"Biri yanlış" mantık soruları:** bilgiler arasında içerme ilişkisi
  ara (ör. 10'a bölünmek 2'ye ve 5'e bölünmeyi de zorunlu kılar);
  başka bir bilgiyi zorunlu kılan bilgi kesin doğrudur, yanlış olan
  bilgi bu zincirin diğer ucundadır.

[← Konu ana sayfasına dön](index.md)

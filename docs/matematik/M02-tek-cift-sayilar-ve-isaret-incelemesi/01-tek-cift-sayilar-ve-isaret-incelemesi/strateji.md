# 🎯 Soru Çözüm Stratejileri — Tek-Çift Sayılar ve İşaret İncelemesi

> Kaynak: Hocanın önerdiği yöntemler + genel best-practice çözüm teknikleri.

## Çift Katsayıdan Başlama Stratejisi

Birden fazla harf içeren bir ifadede yorum yaparken, önce **çift
katsayılı terimden** başla — o terim harften bağımsız olarak kesin
çifttir, bu da diğer harf(ler) hakkında kesin bir bilgiye ulaşmanı sağlar.
Bir harfi bulduktan sonra bir üst/alt ifadeye geçip zinciri devam ettir.

## "İkisi Çift Biri Tek / İkisi Tek Biri Çift" Tipi Sorularda Ortak Harfi Bul

Birden fazla çarpımsal ifadenin ikisi çift biri tek (ya da tersi) verildiğinde,
ifadelerde **ortak geçen harfi** tespit et. O harf çift olursa tüm
ifadeler çift olurdu — bu çelişki, ortak harfin türünü doğrudan verir.

## Kesinlik Yoksa Değer Verme Stratejisi

Soru kökünde "kesinlikle" ifadesi geçmiyorsa, harflere en basit tek (`1`)
ve çift (`2`) değerlerini ata ve ifadeleri doğrudan hesapla. Bu, özellikle
çok harfli ve çok öncüllü sorularda yorum yapmaktan çok daha hızlıdır.

## Amele-Hümayun (Çok İhtimalli) Sorularda Ortak Harf Üzerinden Dallanma

Birden fazla koşulun (`a+b çift`, `a-c tek` gibi) birlikte verildiği
sorularda, koşulların ortak harfini (burada `a`) sabit tutup **her koşulu
ayrı ayrı ihtimallere ayır**, sonra bu ihtimalleri birleştirerek ifadenin
her durumda aynı sonucu verip vermediğini kontrol et. Bir öncül tek bir
ihtimalde bile yanlış çıkarsa, diğer ihtimallere bakmaya gerek kalmadan o
öncül elenir.

## İşaret Sorularında Kuvvet Kısayolunu Uygulama Sırası

İşaretle ilgili bir soruda önce **tek kuvvetli terimlerin kuvvetlerini
sil**, sonra **çift kuvvetli terimleri tamamen sil**. Geriye kalan sade
ifade üzerinden işaret zincirini (çarpım/bölüm pozitif mi negatif mi)
kur.

---

<a id="ornek-1"></a>
## Örnek 1 — Çift Katsayı ile Yorum

**Soru:** `x, y` tam sayı olmak üzere `2x + 5y` ifadesi çift sayıdır.
Buna göre `y` nasıl bir sayıdır?

**Çözüm:**
- `2x` katsayısı çift olduğundan `x`'in ne olduğundan bağımsız olarak
  her zaman **çifttir.**
- `5y` teriminde tek katsayı (`5`) önemsizdir, silinir: geriye `y`
  kalır.
- İfade: çift (`2x`) + `y` = çift. Çiftle toplanınca sonucun çift
  çıkması için `y` de **çift** olmalıdır.
- **Sonuç: `y` çift sayıdır.**

<a id="ornek-2"></a>
## Örnek 2 — Kuvvet ve Katsayı Kısayollarıyla Birlikte Yorum

**Soru:** `a, b` pozitif tam sayılar olmak üzere `a² + 1` çift sayı,
`3b − 1` tek sayıdır. Buna göre `a` ve `b` nasıl sayılardır?

**Çözüm:**
- Kuvvetteki `2`, pozitif tam sayı olduğundan silinir: `a² + 1` yerine
  `a + 1` yorumlanır.
- `a + 1` çift ise, çiftin çift çıkması için `a` **tek** olmalıdır.
- `3b − 1` ifadesinde tek katsayı (`3`) silinir: `b − 1` yorumlanır.
- `b − 1` tek ise, tek katsayısız yorum ile `b` **çift** olmalıdır
  (tekten çift çıkması için `b` çift olmalı).
- **Sonuç: `a` tek, `b` çift sayıdır.**

<a id="ornek-3"></a>
## Örnek 3 — İkisi Çift Biri Tek Tipi Soru

**Soru:** `a, b, c` tam sayılar için `a`, `a×b`, `a×c` ifadelerinden
ikisi çift, biri tek sayıdır. Buna göre bu ifadelerden hangileri
kesinlikle tek sayıdır?

**Çözüm:**
- `a` çift olsaydı, `a×b` ve `a×c` de otomatik çift olurdu — bu, "ikisi
  çift biri tek" bilgisiyle çelişir (üçü de çift olurdu). O hâlde `a`
  **tek**tir.
- `a` tek olduğuna göre, `a×b` ve `a×c`'den ikisinin çift olması için
  `b` ve `c` **çift** olmalıdır.
- Değer vererek doğrula: `a=1, b=2, c=4` → `a=1` (tek), `a×b=2` (çift),
  `a×c=4` (çift). Uyumlu.
- **Sonuç: Sadece `a` kesinlikle tektir.**

<a id="ornek-4"></a>
## Örnek 4 — Kesinlik Yoksa Değer Verme

**Soru:** `m, n` pozitif tam sayı olmak üzere `2m + n`, `(m+n)×p` ve
`n×(m+p)` ifadeleri birer tek sayıdır. Buna göre bu ifadelerden
hangileri tek sayıdır?

**Çözüm:**
- `2m` katsayısı çift olduğundan `2m + n` tek olması için `n`'in
  **tek** olması gerekir.
- Soru kökünde "kesinlikle" ifadesi geçmediği için harflere değer
  verilebilir: `n = 1` (tek).
- `n = 1` iken `(m+n)×p` ifadesinin tek çıkması için `m + p`'nin tek
  olması gerekir (çünkü `1 × (m+p) = m+p`).
- Değer ver: `m = 1, p = 2` → `m+p = 3` (tek, uygun).
- Şimdi ifadeleri hesapla: `m+n+p = 1+1+2 = 4` (çift),
  `n×(m+p) = 1×3 = 3` (tek).
- **Sonuç: Sadece `n×(m+p)` ifadesi tektir** (soru bağlamındaki üçüncü
  ifade).

<a id="ornek-5"></a>
## Örnek 5 — Amele-Hümayun: Ortak Harf Üzerinden Dallanma

**Soru:** `a, b, c` birer tam sayı olmak üzere `a + b` çift sayı,
`a − c` tek sayıdır. Buna göre `a×b×c`, `a + c` ve `a×b + c`
ifadelerinden hangileri her zaman çift sayıdır?

**Çözüm:**
- `a + b` çift olduğundan ya ikisi de çift ya ikisi de tektir (2
  ihtimal): (a çift, b çift) veya (a tek, b tek).
- `a − c` tek olduğundan `a` ve `c`'den biri tek biri çift olmalıdır.
  `a` üzerinden birleştirince 2 senaryo çıkar:
  - Senaryo 1: `a` çift, `b` çift, `c` tek
  - Senaryo 2: `a` tek, `b` tek, `c` çift
- **`a×b×c`:** Senaryo 1'de `a` (çift) çarpanı içeride var → sonuç çift.
  Senaryo 2'de `c` (çift) çarpanı içeride var → sonuç yine çift. Her iki
  senaryoda da içeride en az bir çift çarpan olduğundan bu ifade **her
  zaman çifttir.**
- **`a + c`:** Senaryo 1'de `a` çift, `c` tek → toplam **tek** çıkar.
  Daha ilk senaryoda çift olmadığından bu öncül elenir; ikinci senaryoya
  bakmaya gerek yoktur.
- **`a×b + c`:** Senaryo 1'de `a×b` = çift×çift = çift; `+c` (tek) ile
  toplanınca sonuç **tek** çıkar. İlk senaryoda çift çıkmadığından bu
  öncül de elenir.
- **Sonuç: Sadece `a×b×c` her zaman çifttir.** Bir öncül daha ilk
  senaryoda başarısız olduğunda, zaman kaybetmeden diğer senaryoya
  bakılmadan elenir — bu, çok senaryolu sorularda hız kazandırır.

<a id="ornek-6"></a>
## Örnek 6 — İşaret: Kuvvet Kısayoluyla Belirleme

**Soru:** `a³ × b⁵ × c` ifadesinin işareti pozitiftir, `a² × b⁸`
ifadesinin işareti bilinmemektedir. Kuvvetleri kullanarak `a` ve `b`
hakkında ne söylenebilir?

**Çözüm:**
- `a³`, `b⁵` teriminde kuvvetler tektir → yalnızca kuvvetleri sil,
  işaret aynen `a`, `b` tabanının işaretine eşittir.
- `a²`, `b⁸` teriminde kuvvetler çifttir → bu terimler işarete hiç
  katkı sağlamaz (daima pozitif), tamamen silinir.
- Kalan ifadeden (`a × b × c` pozitif) yorum yapılır: `a`, `b`, `c`
  işaretlerinin çarpımı pozitif olmalıdır.
- **Sonuç: İşaret sorularında kuvveti tek olan terimlerde yalnızca
  kuvvet, çift olan terimlerde ifadenin tamamı silinerek zincir kurulur.**

<a id="ornek-7"></a>
## Örnek 7 — İşaret: Çarpım ve Fark Zinciri

**Soru:** `a, b, c` tam sayılar olmak üzere `a × b × c = 0`,
`a × b < 0` ve `c − b < 0` olduğuna göre `a, b, c`'yi küçükten büyüğe
sıralayınız.

**Çözüm:**
- `a × b × c = 0` olması için en az biri `0` olmalıdır.
- `a × b < 0` (sıfırdan farklı bir sonuç) olduğuna göre `a` ve `b`
  sıfır **değildir**. O hâlde `0` olan **`c`**'dir: `c = 0`.
- `a × b < 0` demek, `a` ve `b`'nin işaretleri **farklı** demektir.
- `c − b < 0` eşitsizliği düzenlenirse `c < b` olur; `c = 0`
  olduğundan `b > 0` (pozitif).
- `a × b < 0` ve `b` pozitif olduğundan `a` **negatif** olmalıdır.
- **Sonuç: `a < c < b`** (negatif < sıfır < pozitif sıralaması).

[← Konu ana sayfasına dön](index.md) · [⚠️ Yaygın Hatalar →](yaygin-hatalar.md)

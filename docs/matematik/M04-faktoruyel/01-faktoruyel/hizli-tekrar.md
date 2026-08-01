# Hızlı Tekrar — faktöriyel

- **Tanım:** `n! = 1×2×3×...×n`; yalnızca doğal sayılarda tanımlıdır,
  negatiflerde tanımsızdır. `0! = 1` (özel kabul; kombinasyon formülüyle
  ispatlanır).
- **Ardışık açılım:** `n! = n×(n-1)×...×(k+1)×k!` — sayının kendisinden
  başlanıp birer birer azalarak durulan yerde faktöriyel konur.
- **Sadeleştirme (bölme):** `a!/b! = (b+1)×(b+2)×...×a` (büyükten
  küçüğe, küçükten sonraki çarpanlar kalır).
- **Toplama/çıkarmada parantez:** en küçük faktöriyeli parantezine al;
  her terimden "kendisinden sonraki çarpanlar" kalır, hiçbir şey
  kalmıyorsa `1` yaz.
- **Çarpma varsa parantez alınmaz:** `7 × 6!` gibi bir çarpım
  faktöriyel parantezine sokulamaz; parantez alma yalnızca
  toplama/çıkarmada geçerlidir.
- **Ardışık azalan diziyi faktöriyele çevirme:**
  `a×(a-1)×...×k = a!/(k-1)!` (en büyük! / en küçüğün-bir-eksiği!).
- **`A!=k×B!` denklemleri çok çözümlü olabilir:** `k`'yı ardışık
  çarpanlara farklı biçimlerde ayırmayı dene, her ayırma ayrı bir çözüm.
- **Asal tabanda üs (Legendre):** `n`'i tabana sürekli böl, bölümleri
  topla (kalanlar önemsiz).
- **Asal olmayan tabanda üs:** önce asal çarpanlara ayır, en az bulunan
  asalın adedini al.
- **Sondan kaç basamağı `0`:** `n`'i sürekli `5`e böl, bölümleri topla
  (`2` her zaman `5`ten fazla olduğu için `5` sınırlayıcıdır).
- **Toplama/çarpma/bölmede sıfır sayısı:** toplamada küçüğü al, çarpmada
  topla, bölmede çıkar.
- **Ardışık faktöriyellerin toplamında** doğrudan küçüğü almak
  **yanlıştır** — parantez aç, yeni oluşan `5` çarpanlarını da say
  (`24!+23! = 23!×25`, `25` ek `5²` getirir).
- **`n!-1`in sondan kaç basamağı `9`:** `n!`in sondan kaç basamağının
  `0` olduğuna eşittir (bir sayıdan `1` çıkınca `0`lar `9`a döner).
- **Negatif faktöriyel kısıtı:** `(x-a)!` ve `(a-x)!` gibi birbirinin
  tersi ifadeler aynı anda geçiyorsa, genelde yalnızca ikisini de
  sıfırlayan tek değer (`x=a`) geçerlidir.

[← Konu ana sayfasına dön](index.md)

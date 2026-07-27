# 📘 Teorik Bilgiler — İşlem Yeteneği

> Kaynak: Değişmeyen matematik kuralları (tanımlar, kurallar, formüller). Hoca anlatımından bağımsızdır.

## Toplama – Çıkarma İşaret Kuralı

- **Aynı işaretli** sayılar toplanır, sonucun önüne ortak işaret yazılır.
  - `(+7) + (+5) = +12`
  - `(-3) + (-5) = -8`
- **Farklı işaretli** sayılarda büyükten küçük çıkarılır, sonucun önüne
  **mutlak değeri büyük olan sayının işareti** yazılır.
  - `-5 + 9 = +4` (9 büyük, işareti +)
  - `-12 + 7 = -5` (12 büyük, işareti −)

## Çarpma – Bölme İşaret Kuralı

- Aynı işaretliler → sonuç **pozitif**
- Farklı işaretliler → sonuç **negatif**

## Parantez Önündeki İşaretin Dağıtılması

- Parantezin önünde **eksi (−)** varsa, parantez içindeki **her terimin
  işareti değişir**: `−(a − b + c) = −a + b − c`
- Parantezin önünde **artı (+)** varsa, içindeki hiçbir işaret değişmez:
  `+(a − b + c) = a − b + c`

## Ortak Çarpanı Parantezine Alma

- `ax + bx = x(a + b)` — ortak çarpan (`x`) dışarı alınır, geri kalan
  parantez içine yazılır.
- Bir terimden geriye **hiçbir şey kalmıyorsa**, o terimin yerine **1**
  yazılır (her terim örtük olarak kendisiyle çarpılan bir 1'e sahiptir):
  `ax + x = x(a + 1)`

## İşlem Önceliği

Bir işlemde uygulama sırası:

1. **Parantez içi**
2. **Üslü ifadeler (kuvvet alma)**
3. **Çarpma / Bölme** (soldan sağa)
4. **Toplama / Çıkarma** (soldan sağa)

> **Kritik nüans:** Çarpma ile bölme arasında öncelik yoktur; toplama ile
> çıkarma arasında da öncelik yoktur. Bu işlem çiftleri kendi aralarında
> **soldan sağa, sırayla** yapılır — hangisi önce geliyorsa o uygulanır.

## Üslü Sayılar

- Pozitif bir sayının tüm kuvvetleri pozitiftir.
- Negatif bir tabanın kuvveti:
  - **Tek** kuvvette sonuç **negatif** kalır (parantez içi/dışı fark etmez).
  - **Çift** kuvvette sonuç **pozitif** olur — **yalnızca kuvvet, tabanla
    birlikte parantezin içindeyse.**
    - `(-2)^4 = 16` (taban parantez içinde, çift kuvvet → pozitif)
    - `-2^4 = -16` (önce `2^4 = 16` alınır, sonra baştaki eksi işareti
      uygulanır; kuvvet tabanı değil yalnızca `2`'yi kapsar)
- **Sıfırıncı kuvvet:** `a^0 = 1` (`a ≠ 0`). `0^0` tanımsız/belirsiz kabul edilir.
  - `0` da çift bir sayı olduğundan aynı parantez kuralı geçerlidir:
    `(-2)^0 = 1` iken `-2^0 = -1`.
- **1'in bütün kuvvetleri 1'dir:** `1^n = 1` (her `n` için).
- **-1'in kuvveti:** çift ise `+1`, tek ise `-1`.

## Harf Yerine Sayı Koyma Kuralı

Bir ifadedeki harfin yerine (özellikle **negatif**) bir değer yazılırken,
o değer mutlaka **parantez içine** konmalıdır; aksi hâlde üslü/işaretli
ifadelerde hata oluşur.

- `a² + a` ifadesinde `a = -2` için: `(-2)² + (-2) = 4 - 2 = 2`

[← Konu ana sayfasına dön](index.md) · [💡 Pratik Bilgiler →](pratik.md)

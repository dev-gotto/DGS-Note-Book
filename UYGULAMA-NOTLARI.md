# Uygulama Notları

Bu zip, repoya doğrudan uygulanacak 4 dosya değişikliği içerir. Dizin yapısı repo ile birebir aynıdır; dosyaları aynı adlarla kopyalayıp üzerine yazmanız yeterlidir.

## Değiştirilen / Eklenen Dosyalar

1. `docs/matematik/M01-islem-yetenegi.md` — **üzerine yazılacak**
   Eksik 6 bölüm eklendi (Pratik Bilgiler, Soru Çözüm Stratejileri, Yaygın Hatalar, Çözümlü Örnekler, Hızlı Tekrar, Kaynak, Değişiklik Geçmişi) + metadata.yml uyumlu front-matter.

2. `docs/index.md` — **üzerine yazılacak**
   Landing page genişletildi: proje amacı, konu durumu (M01/M02/G01 ilerleme listesi), kullanım rehberi.

3. `CHANGELOG.md` — **üzerine yazılacak**
   Yeni `v0.9.0 Content Structure Update` girişi en üste eklendi, eski `v0.8.1 Hotfix` girişi korundu.

4. `mkdocs.yml` — **üzerine yazılacak**
   Nav yapısı aynı kaldı (Geometri henüz içerik olmadığı için nav'a eklenmedi — eklenirse mkdocs build hata verir). Geometri eklenmesi gerektiğinde nereye ekleneceğini gösteren bir yorum satırı eklendi.

## Elle Yapmanız Gereken Bir İşlem

- Kök dizindeki **`commit-message.txt`** dosyasını silmenizi öneririm. `.github/commit-template.txt` ile çakışıyor ve iki farklı örnek mesaj içeriyorlar. Bu zip'e dahil edilmedi çünkü "silinecek" bir dosya zip içine konularak ifade edilemiyor — repoda elle silmeniz gerekiyor.

## Önerilen Commit Mesajı

```
docs(M01): konu tamamlandı, şablon uyumu sağlandı

- M01 tüm şablon bölümleriyle tamamlandı
- metadata front-matter eklendi
- docs/index.md landing page genişletildi
- CHANGELOG v0.9.0 girişi eklendi
- mkdocs.yml Geometri notu eklendi
```

## Sonraki Adım

Bu paket commit edildikten sonra derin analiz için önerdiğim başlıklar:
- M01 içeriğinin DGS müfredatına göre doğruluk/kapsam kontrolü (bir konu uzmanı gözüyle)
- templates/metadata.yml alanlarının (previous/next) M02 eklendiğinde nasıl bir zincir oluşturacağının planlanması
- GitHub Actions workflow'unun mkdocs.yml'deki `strict: true` gibi bir ayarla nav/dosya tutarsızlıklarını build zamanında yakalayıp yakalamayacağının değerlendirilmesi

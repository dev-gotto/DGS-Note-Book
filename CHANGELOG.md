# CHANGELOG

## v0.9.0 Content Structure Update

### Yapılanlar
- M01 İşlem Yeteneği dosyası şablonla (templates/konu.md) tam uyumlu hale getirildi: Pratik Bilgiler, Soru Çözüm Stratejileri, Yaygın Hatalar, Çözümlü Örnekler, Hızlı Tekrar, Kaynak ve Değişiklik Geçmişi bölümleri eklendi.
- M01 dosyasına metadata.yml şablonuna uygun front-matter eklendi (id, title, status, version, previous, next, references).
- docs/index.md genişletildi: proje amacı, konu durumu (Matematik/Geometri ilerleme listesi) ve kullanım rehberi eklendi.
- Kök dizindeki commit-message.txt ile .github/commit-template.txt arasındaki çakışma tespit edildi; .github/commit-template.txt referans şablon olarak kabul edilmesi, kök dizindeki commit-message.txt dosyasının kaldırılması önerilir (bkz. UYGULAMA-NOTLARI.md).

## v0.8.1 Hotfix

### Yapılanlar
- GitHub Actions için contents: write izni eklendi.
- mkdocs.yml nav güncellendi.
- PRE_COMMIT_CHECKLIST eklendi.
- Teslim standardı AI_CONTEXT ve PROJECT_RULES dosyalarına eklendi.

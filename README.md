# FuresTube – bağımsız video sitesi görünüm testi

Canlı test: https://youtubefur.netlify.app

Bu bağımsız, statik önizleme sitesi YouTube ana sayfasındaki küçük kapak görsellerini ve video izleme sayfasını masaüstü/mobil boyutlarında değerlendirmek içindir. Resmi YouTube hizmeti değildir. Gerçek kullanıcı hesabı, yorum veya görüntüleme verisi içermez.

## Kullanım
- Ana sayfa: `/#home`; video: `/#watch`.
- Kapak yükle: bir görsel seçin; 1280×720 JPEG önizlemesi tarayıcıda yerel olarak saklanır. Kapağı sıfırla düğmesi yerel seçimi siler.
- Paylaşılan varsayılan kapak için `media/thumbnail-tr.jpg` dosyasını GitHub'a ekleyin. Yoksa `media/poster.jpg` kullanılır.
- Tema düğmesiyle açık/koyu görünümü karşılaştırın.
- Örnek video kartları ve istatistikler yalnızca yerleşim testidir.
- Türkçe altyazı başlangıçta kapalıdır; oynatıcıdan açılabilir.

## Dosyalar
- `index.html`: tek dosyalı, bağımlılıksız HTML/CSS/JS.
- `media/kahve-001-tr.mp4`: mevcut 720p kurgu (7:35).
- `media/kahve-001-tr.tr.vtt`: Türkçe altyazı.
- `media/poster.jpg`: mevcut yedek kapak.
- `netlify.toml`: yayın ayarları.
- `AGENTS.md`: ajanlar için değişiklik ve doğrulama kuralları.

İçerik üretim kaynağı: https://github.com/furesat/youtube-studio-

Yerelde: `python3 -m http.server 8000`, ardından http://localhost:8000. Netlify mevcut `main` branch'inden yayınlanır; değişiklik sonrası canlı deploy durumunu kontrol edin. Site noindex kullanır; bu erişim kontrolü değildir. Gizli içerik için ayrıca erişim koruması gerekir.

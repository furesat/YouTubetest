# AGENTS.md – FuresTube test sitesi

## Amaç
Bu repo, gerçek videoların ve kapakların YouTube benzeri ortamda değerlendirilmesi için bağımsız test sitesidir. Kanal üretim dosyalarının ana deposu https://github.com/furesat/youtube-studio- adresidir. Bu repo ise yalnızca önizleme/yayın katmanıdır.

## Değişiklik kuralları
- Mevcut Netlify projesi: youtubefur. URL: https://youtubefur.netlify.app. Yeni site oluşturma.
- Önce mevcut dosyaları ve son deploy durumunu oku; eşzamanlı değişiklikleri ezme.
- YouTube benzeri 16:9 kartlar, başlık, kanal, süre etiketi, masaüstü grid, mobil akış, izleme sayfası ve açık/koyu temayı koru. Gerçek YouTube'a giriş, kimlik bilgisi veya gerçek kullanıcı verisi ekleme. Test ibaresini koru.
- Örnek kartlar ve istatistikler gerçek veri gibi sunulmasın.
- Mevcut video MP4 ve VTT dosyalarını kullanıcı istemedikçe değiştirme/silme. CC ilk açılışta kapalı olmalı.
- Kalıcı kapak: `media/thumbnail-tr.jpg`, 1280×720, 16:9, tercihen 2 MB altında. Orijinal görseli üretim reposunda koru. Tarayıcı yüklemesi yalnız yerel önizlemedir; GitHub'a yazmaz.
- Yeni video eklerken ayrı MP4/VTT/thumbnail yolları ve gerçek süre/başlık kullan. Mevcut videoları koru.
- Statik ve bağımlılıksız yapıyı koru; yeni servis, ücretli özellik, hesap veya takip kodu ekleme.
- noindex erişim koruması değildir; gizli materyali açık repoya yükleme.

## Doğrulama
1. Masaüstü (1440×900) ve mobil (390×844) ana sayfa/izleme ekranlarını gerçek tarayıcıda kontrol et.
2. Kapak kırpılması, başlık okunurluğu, yatay taşma ve koyu tema kontrolü.
3. Videoyu başlat/durdur, ses, ileri sarma ve CC aç/kapa testleri.
4. Kapak yükleme, yenilemeden sonra yerel saklama ve sıfırlama testleri.
5. GitHub commit SHA ve Netlify production deploy durumunu doğrula; eski deploy ile karıştırma.
6. Çalıştırılmayan testleri açıkça NOT_RUN olarak bildir. Yapılmayan işlemleri tamamlanmış gibi sunma.

## Rapor
Değişen dosyalar, commit SHA, canlı URL, test sonuçları ve engelleri kısa şekilde bildir.

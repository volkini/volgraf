# Claude oturum notları — 8 Temmuz 2026

Volgraf sitesi üzerine yapılan çalışmanın özeti ve yapılacaklar. (Bu dosya `claude-notlar`
branch'indedir, siteye dahil değildir.)

## Mevcut durum

- Site **yayında**: https://volkini.github.io/volgraf/ — GitHub Pages, `main` branch'ten
  otomatik Jekyll derlemesi yapıyor. Push = yayınlamak.
- Yapı: çok sayfalı Jekyll sitesi (ana sayfa, /projects/, /shop/, proje detay sayfaları).
  Arayüz iki dilli (EN/TR), içerik SEO için İngilizce. SEO altyapısı hazır
  (jekyll-seo-tag, jekyll-sitemap, JSON-LD).
- Proje ekleme: https://app.pagescms.org — GitHub hesabıyla giriş → volkini/volgraf seç →
  Projects → Add entry. Panel doğrudan repoya commit atar, site 1-2 dk'da güncellenir.

## volgraf.com durumu

- Alan adı **25 Haziran 2026'da Cloudflare Registrar üzerinden tescillenmiş**.
  Sahibi WHOIS'te gizli; Volkan satın alıp almadığını hatırlamıyor.
- DNS kayıtları şu an boş (site bağlı değil).
- Claude oturum geçmişinde "volgraf" araması yapıldı: alan adı Claude ile alınmamış.

### Sahiplik kontrolü (yarın yapılacak)

1. **dash.cloudflare.com** → giriş dene (iş ve kişisel e-postalarla, gerekirse şifre
   sıfırlama). Hesapta volgraf.com görünüyorsa alan adı bizde. En kesin yöntem.
2. E-postalarda ara: `volgraf`, `cloudflare` (spam dahil). Kayıt maili
   notify.cloudflare.com adresinden gelir.
3. Kart ekstresinde 25 Haziran tarihli ~10-11 USD "CLOUDFLARE" çekimi ara.
4. Hiçbirinde iz yoksa alan adı başkasının → alternatif uzantı (volgraf.net, .co)
   veya sahibine satın alma teklifi konuşulacak.

## Alan adı doğrulanınca yapılacaklar

1. Cloudflare → volgraf.com → DNS → Records, şu kayıtlar eklenecek (hepsi "DNS only",
   gri bulut — GitHub'ın SSL sertifikası üretebilmesi için proxy kapalı olmalı):

   | Tip   | Ad  | Değer            |
   |-------|-----|------------------|
   | A     | @   | 185.199.108.153  |
   | A     | @   | 185.199.109.153  |
   | A     | @   | 185.199.110.153  |
   | A     | @   | 185.199.111.153  |
   | CNAME | www | volkini.github.io |

2. Evdeki bilgisayarda hazır bekleyen commit push'lanacak (`main` branch'inde,
   commit `59e9ccc` "Move site to custom domain volgraf.com": CNAME dosyası,
   _config.yml url/baseurl, robots.txt, Pages CMS görsel yolu).
   **DNS eklenmeden push'lanmamalı** — site geçici olarak erişilemez olur.
3. GitHub → repo Settings → Pages: Custom domain alanında volgraf.com görünecek,
   DNS doğrulanınca **Enforce HTTPS** işaretlenecek. Eski github.io adresi otomatik
   yeni alan adına yönlenir.

## Yayın sonrası SEO adımları

1. **Google Search Console**: "Domain" tipi mülk ekle (Cloudflare'e TXT kaydıyla doğrulama),
   `https://volgraf.com/sitemap.xml` gönder.
2. Placeholder görselleri gerçek CAD render/fotoğraflarla değiştir (+ açıklayıcı alt
   metinler). Ana sayfadaki sosyal paylaşım görseli (og:image, 1200×630) de placeholder.
3. Her yeni proje sayfası uzun kuyruklu aramalar için giriş kapısı — detaylı yazmaya devam.
4. İleride: Tailwind CDN yerine derlenmiş CSS (sayfa hızı), Bing Webmaster Tools.

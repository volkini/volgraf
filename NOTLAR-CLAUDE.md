# Claude oturum notları

Volgraf sitesi üzerine yapılan çalışmanın özeti ve yapılacaklar — **iki bilgisayar
arasındaki senkronizasyon dosyası.**

**Nasıl kullanılır:** Dosya `main` branch'indedir (Jekyll `exclude` listesinde, siteye
dahil edilmez). Her Claude oturumu sonunda o günkü durum ve yapılacaklar buraya tarihli
bölüm olarak eklenir ve push'lanır. Yeni oturuma başlarken önce `git pull` yapılır ve
Claude'dan bu dosyayı okuması istenir — kaldığın yerden devam etmenin yolu budur.

---

## GUNCEL YAPILACAKLAR — son guncelleme: 14 Temmuz 2026

Sirali liste; ustteki once. (V) = Volkan yapacak, (C) = Claude yapacak.

- [ ] 1. (V) **Form aktivasyonu**: /contact/ sayfasindan deneme gonderisi yap,
      volkini@gmail.com'a gelen formsubmit.co mailinde "Activate"e tikla.
      Yapilmazsa musteri mesajlari ulasmaz.
- [ ] 2. (V) **partkraft.com satin al** (Porkbun/Namecheap) + AYNI GUN Instagram
      @partkraft ve YouTube @partkraft hesaplarini ac. (13 Tem itibariyle ucu de bos.)
- [ ] 3. (C) Alan adi alininca: site+repo PartKraft'a tasinacak, DNS baglanacak,
      Enforce HTTPS, Google Search Console + sitemap gonderimi.
- [ ] 4. (V) **CV'yi Claude'a gonder** -> (C) /about/ doldurulacak: araclar/yazilimlar,
      deneyim, foto, CV indirme butonu.
- [ ] 5. (V) Gercek proje gorselleri (Pages CMS'ten yukle) -> (C) vaka calismasi
      formatina gecis (problem-yaklasim-sonuc). Volkan: "en son is" dedi ama
      Upwork/musteri trafigi oncesi sart.
- [ ] 6. (V) GrabCAD profili ac + en iyi modelleri yukle -> (C) footer'a link
      (_config.yml -> social.grabcad).
- [ ] 7. (V) LinkedIn profili (EN) -> (C) profil metinlerini yazar, siteye baglar
      (social.linkedin). Ardindan Upwork profili.
- [ ] 8. Reklam EN SON (site olgunlasinca). AdSense YOK — kesin karar.

### Tamamlananlar
- [x] Cok sayfali Jekyll sitesi + SEO altyapisi (8 Tem)
- [x] Pages CMS yonetim paneli (8 Tem)
- [x] volgraf.com sahiplik arastirmasi — bizim degil (13 Tem)
- [x] Marka arastirmasi — PartKraft secildi, simdilik (13 Tem)
- [x] /services/, /about/ iskeleti, /contact/ teklif formu, /thanks/ (14 Tem)
- [x] Iletisim e-postasi volkini@gmail.com'a duzeltildi + tam site kontrolu (14 Tem)

---

## Oturum: 8 Temmuz 2026 (ev)

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

---

## Oturum: 8 Temmuz 2026 (is bilgisayari)

- `claude-notlar` branch'i `main`'e alindi ve bu dosya senkronizasyon dosyasi yapildi
  (Jekyll exclude'a eklendi, sitede yayinlanmaz). `claude-notlar` branch'i silindi.
- volgraf.com DNS kontrol edildi: Cloudflare NS (rex/clarissa), A kaydi yok - not
  dosyasindaki durumla ayni, degisiklik yok.
- **Bekleyen isler (oncelik sirasiyla):**
  1. Cloudflare hesap kontrolu ile volgraf.com sahipligi netlestirilecek (yukaridaki
     "Sahiplik kontrolu" adimlari).
  2. Sahiplik dogrulanirsa: once Cloudflare'e DNS kayitlari, SONRA evdeki bilgisayardaki
     59e9ccc commit'i push'lanacak. DIKKAT: ev bilgisayari push'tan once `git pull`
     yapmali (main'e bu oturumda yeni commit'ler eklendi, 59e9ccc _config.yml'i
     degistirdigi icin kucuk bir merge gerekebilir).
  3. Google Search Console kaydi (alan adi netlesince "Domain" tipi mulk olarak).
  4. Placeholder gorseller gercek render/fotograflarla degistirilecek (Pages CMS'ten).

---

## Oturum: 13 Temmuz 2026 (is bilgisayari) - ALAN ADI SONUCU

- **volgraf.com bizim degil.** Volkan tum kontrolleri yapti: Cloudflare hesabi yok,
  e-postalarda iz yok. Alan adini 25 Haziran'da baskasi tescillemis (park sayfasi da
  yok, A kaydi bos).
- **ONEMLI: Evdeki 59e9ccc commit'i ("Move site to custom domain volgraf.com")
  ARTIK PUSH'LANMAMALI ve silinmeli** (`git reset --hard origin/main` ile - once
  baska degisiklik olmadigindan emin ol). Alan adi degisince yeni yapilandirmayi
  is bilgisayarindaki oturum hazirlayacak.
- Alternatif uzantilar kontrol edildi (RDAP), hepsi BOS: volgraf.net, .org, .co,
  .io, .dev, .me, .xyz, .engineer, .com.tr (com.tr icin trabis.gov.tr'den teyit
  onerilir).
- Karar bekleniyor: hangi uzanti alinacak. Oneri: volgraf.net (uluslararasi satis +
  EN SEO hedefine uygun) ve istege bagli yaninda volgraf.com.tr (Turkiye guveni).

---

## Oturum: 13 Temmuz 2026 (is bilgisayari) - MARKA ARASTIRMASI

Yeni isim aranyor (Volgraf sart degil, .com'u bos bir isim istendi). 36 aday tarandi:
.com (Verisign RDAP) + Instagram (tarayici ile) + YouTube + marka cakismasi aramasi.

### Finalistler - hepsinde .com + Instagram + YouTube BOS (13 Temmuz itibariyle)

1. **PartKraft** (partkraft.com) - ONERILEN. Kisa (9 harf), TR+EN kolay telaffuz/yazim,
   uretim havasi guclu, cakisma yok. Turk musteri de hedefse en iyisi.
2. **ChamferWorks** (chamferworks.com) - yakin ikinci. En guclu muhendislik sinyali,
   ama Turkce konusana telaffuzu zor. ABD'de "Chamfer Woodworking" var (farkli isim
   ve sektor, dusuk risk).
3. **SnapFitWorks** (snapfitworks.com) - 3D print dosya satisina en uygun cagrisim,
   ama uzun ve "print dukkani" gibi durabilir.
4. MillAndMold - ahsap isi cagrisimi + benzer isimli firmalar. Onerilmez.
5. DraftAndMill - pub/bira evi gibi okunabiliyor. Onerilmez.

### Elenenler (.com bos ama Instagram alinmis)
partdraft, milldraft, mekaforge, torqform (torqform ayrica aktif Kore markasi).

### Isim secilince yapilacaklar
1. Ayni gun: .com satin al (Porkbun/Namecheap) + Instagram + YouTube hesaplarini ac.
2. Claude'a soyle: sitedeki tum marka metinleri, logo, _config.yml, repo adi ve
   Pages CMS yapilandirmasi yeni isme cevrilecek; alan adi GitHub Pages'e baglanacak
   (DNS kayitlari + CNAME + Enforce HTTPS); Google Search Console kaydi yapilacak.
3. GitHub repo adi degisirse eski volkini.github.io/volgraf adresi otomatik yonlenir
   (GitHub rename yonlendirmesi), Pages CMS'te repo yeniden secilir.

---

## Oturum: 14 Temmuz 2026 (is bilgisayari) - HIZMET SITESINE DONUSUM + YOL HARITASI

Hedef netlesti: site, ABD/Avrupa (belki Asya) kaynakli uzaktan CAD-CAE isi cekecek.
Marka karari simdilik PartKraft (alan adi HENUZ ALINMADI - alinana kadar site Volgraf
kalacak, gecis tek seferde yapilacak).

### Bu oturumda siteye eklenenler
- /services/ - 4 hizmet: Parca ve Urun Tasarimi, Makina Tasarimi, Uretim Resimleri
  (GD&T), Uzaktan Montaj Destegi + "nasil calisir" + guven sinyalleri (NDA, IP devri,
  saat dilimi, Ingilizce).
- /contact/ - teklif formu (formsubmit.co uzerinden site.email adresine gider).
  ONEMLI: ILK form gonderiminde formsubmit.co aktivasyon maili atar - mailde
  "Activate" tiklanmali, yoksa form calismaz. E-posta _config.yml'de: email alani.
- /about/ - iskelet hazir; CV gelince Araclar/Deneyim bolumleri doldurulacak,
  foto + CV indirme butonu eklenecek.
- /thanks/ - form sonrasi tesekkur sayfasi.
- Nav: Services / Projects / 3D Files / About / Get a Quote. Ana sayfa: "musait"
  rozeti + Get a Quote birincil CTA. Footer: LinkedIn/GrabCAD/Instagram linkleri
  (_config.yml social alani; bos oldugu surece gizli).

### YOL HARITASI (oncelik sirasi)
1. partkraft.com + @partkraft Instagram + YouTube al (AYNI GUN). Sonra Claude'a
   soyle: site+repo yeni isme tasinacak, DNS baglanacak, Search Console kurulacak.
2. Volkan CV gonderecek -> About sayfasi doldurulacak (araclar, deneyim, foto, CV pdf).
3. Formun ilk aktivasyonu: /contact/ sayfasindan test gonderimi yap, gelen mailde
   Activate'e tikla.
4. Gercek proje gorselleri (Pages CMS'ten) + vaka calismasi formatina gecis. (Volkan: "en son is")
5. GrabCAD profili ac, en iyi modelleri yukle, footer'a linki ekle (_config.yml social.grabcad).
6. LinkedIn profili (EN) kur/guncelle, siteye bagla (social.linkedin). Upwork profili ac.
7. Reklam EN SON: site olgunlasip referans birikince konusulacak. AdSense YOK (karar).

- DUZELTME (14 Tem): Iletisim e-postasi volkini@gmail.com olarak degistirildi
  (volkan@aykimaluminium.com DEGIL). Form aktivasyon maili gmail'e gelecek.
  Tam site kontrolu yapildi: 11 sayfa 200, eski adres temizlendi, SEO etiketleri
  ve site haritasi tam, WhatsApp/dil degistirici canlida dogrulandi, konsol hatasiz.

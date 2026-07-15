# PartKraft içerik kanalları — yayın kaydı

`social-media-manager` Claude skill'i tarafından tutulur. Bilim-teknoloji
içerik kanallarının (EN + TR) yayınlanan/zamanlanan her içeriği buraya
eklenir — **en yeni en üstte**. Dosya bu repoda yalnızca iki bilgisayar
arasında git senkronu için durur (Jekyll exclude'da, siteyle ilgisi yok).
Her kayıttan sonra commit + push yapılır.

**Kayıt formatı:**

```
## 2026-07-20 — EN — YouTube Shorts
- **Konu:** JWST mirror alignment precision
- **Durum:** published | scheduled (2026-07-22T18:00Z) | failed | taslak
- **Metin/başlık (ilk satır):** James Webb's Mirrors Are Aligned to 10 Nanometers...
- **Görsel/video:** Blotato AI video (id: ...)
- **Canlı URL:** https://youtube.com/shorts/...
- **postSubmissionId:** abc-123
```

`scheduled` kayıtların canlı URL'si sonradan doldurulur — her oturum başında
zamanı geçmiş bekleyen kayıtları kontrol et, URL'leri işle, hataları raporla.
Konu tekrarını önlemek için yeni hafta planlanırken bu dosya taranır.

---

*(Henüz yayınlanmış içerik yok.)*

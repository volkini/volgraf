# Sosyal medya yayın kaydı

`social-media-manager` Claude skill'i tarafından tutulur. Yayınlanan her post
buraya eklenir — **en yeni en üstte**. Dosya `main`'dedir ve Jekyll exclude
listesindedir (siteye dahil edilmez); iki bilgisayar arasında git ile senkron
olur. Her kayıttan sonra commit + push yapılır.

**Kayıt formatı:**

```
## 2026-07-20 — LinkedIn
- **Durum:** published | scheduled | failed | taslak
- **Metin (ilk satır):** A client's welded bracket assembly had 14 parts...
- **Görsel:** braket-render.png (Blotato media URL)
- **Canlı URL:** https://www.linkedin.com/posts/...
- **postSubmissionId:** abc-123
```

`scheduled` kayıtların canlı URL'si sonradan doldurulur — oturum başında
bekleyen kayıt var mı diye kontrol et.

---

*(Henüz yayınlanmış post yok.)*

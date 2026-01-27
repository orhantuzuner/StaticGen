# 🌐 StaticGen - Multi-Language Static Site Generator

SEO-friendly, çoklu dil destekli şirket web sitesi üreticisi. Sadece JSON dosyasını düzenleyerek profesyonel web sitesi oluşturun.

## ✨ Özellikler

- 🌍 **Çoklu Dil Desteği** (TR, EN, DE) - Kolayca yeni diller eklenebilir
- 🎯 **SEO-Friendly** - Hreflang tags, meta tags, sitemap
- 📱 **Responsive** - Mobil uyumlu Tailwind CSS
- 🚀 **Statik Export** - Sunucu gerekmez, hızlı hosting
- 🔄 **Hiyerarşik Ürün Yapısı** - Sınırsız derinlik
- 🎨 **Kolay Özelleştirme** - Tek JSON dosyası

## 🚀 Hızlı Başlangıç
```bash
# Projeyi klonla
git clone https://github.com/KULLANICI_ADIN/staticgen-nextjs.git
cd staticgen-nextjs

# Bağımlılıkları yükle
npm install

# Geliştirme modunda çalıştır
npm run dev

# http://localhost:3000/tr
```

## 📁 Proje Yapısı
```
staticgen-project/
├── locales/          # Dil dosyaları (tr.json, en.json, de.json)
├── components/       # React bileşenleri
├── lib/             # Yardımcı fonksiyonlar
├── pages/           # Next.js sayfaları
└── public/          # Statik dosyalar
```

## 🎨 Özelleştirme

### Dil Dosyalarını Düzenle

`locales/tr.json`, `locales/en.json`, `locales/de.json` dosyalarını düzenleyerek içerikleri değiştirin.
```json
{
  "site": {
    "title": "Şirket Adınız",
    "description": "Açıklama"
  },
  "products": {
    "items": [
      {
        "id": "urun1",
        "slug": "urun-slug",
        "name": "Ürün Adı",
        "description": "Ürün açıklaması",
        "children": [...]
      }
    ]
  }
}
```

### Yeni Dil Eklemek

1. `locales/fr.json` oluştur
2. `next.config.js`'e ekle:
```javascript
i18n: {
  locales: ['tr', 'en', 'de', 'fr'],
  defaultLocale: 'tr'
}
```

## 📦 Production Build
```bash
# Statik HTML üret
npm run build

# out/ klasörü oluşur - deploy edilmeye hazır
```

## 🚀 Deployment

### Vercel
```bash
npm i -g vercel
vercel
```

### Netlify
```bash
npm run build
netlify deploy --prod --dir=out
```

### GitHub Pages
```bash
npm run build
# out/ klasörünü gh-pages branch'ine push edin
```

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Commit yapın (`git commit -m 'Add amazing feature'`)
4. Push edin (`git push origin feature/amazing-feature`)
5. Pull Request açın

## 📝 Lisans

MIT License - Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## 👨‍💻 Geliştirici

**Adınız** - [@github_username](https://github.com/github_username)

## 🙏 Teşekkürler

- [Next.js](https://nextjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [React](https://reactjs.org/)

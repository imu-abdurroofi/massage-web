# 🌿 Ummu Amirah Massage - Website

Website profesional untuk layanan pijat dan spa home service dengan desain modern, responsive, dan user-friendly.

![Version](https://img.shields.io/badge/version-2.0-green)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## ✨ Features

- 🎨 **Modern UI/UX Design** - Clean, professional, dan mudah digunakan
- 📱 **Fully Responsive** - Perfect di semua device (mobile, tablet, desktop)
- 🌙 **Dark Mode** - Toggle theme dengan smooth transition
- 🍃 **Falling Leaves Animation** - Subtle natural animation
- 💰 **20+ Layanan** - Lengkap dengan harga dan durasi
- 🔖 **Price Highlight** - Badge "Harga Baru" untuk layanan dengan update harga
- ⚡ **Fast & Lightweight** - Pure HTML, CSS, JavaScript (no framework)
- ♿ **Accessible** - WCAG AAA compliant untuk touch targets
- 🎯 **SEO Ready** - Semantic HTML dan meta tags

---

## 🚀 Quick Start

### Cara Menggunakan

1. **Clone atau Download repository**
   ```bash
   git clone https://github.com/username/massage-web.git
   cd massage-web
   ```

2. **Buka di browser**
   - Double-click `index.html`
   - Atau gunakan Live Server di VS Code

3. **Edit konten**
   - Edit `index.html` untuk konten
   - Edit `style.css` untuk styling
   - Edit `script.js` untuk functionality

### Struktur Folder

```
massage-web/
├── index.html              # Main HTML file
├── style.css               # Stylesheet dengan responsive design
├── script.js               # JavaScript untuk interactivity
├── img/
│   └── logo.png           # Logo website
├── README.md              # Dokumentasi ini
└── REVISI_CHANGELOG.md    # Changelog detail revisi
```

---

## 📋 Sections

### 1. **Hero Section**
- Headline yang menarik
- Call-to-action button
- Falling leaves animation
- Responsive background

### 2. **Services**
Dua kategori layanan:

#### Massage & Hijamah/Bekam Therapy
- Bekam, Inframerah, Guasha (Rp200.000)
- Bekam, Back Massage, Inframerah (Rp300.000) ⭐ **Harga Baru**
- Bekam & Hot Stone Massage (Rp400.000) ⭐ **Harga Baru**
- Bekam & Aromatherapy Massage (Rp400.000)
- Bekam Promil (Rp200.000)

#### Body Treatments
- Javanese Massage (Rp200.000)
- Mom Day Spa (Rp400.000)
- Sport Massage (Rp300.000)
- Pijat, Totok Wajah & Punggung (Rp400.000) ⭐ **Harga Baru**
- Pulen Legit Massage (Rp400.000)
- Pregnancy Massage (Rp200.000)
- Laktasi & Oksitosin Massage (Rp400.000)
- Baby/Kids Massage (Rp150.000)
- Body Scrub (Rp120.000)
- Detoxifying Massage (Rp450.000)
- Slimming Massage (Rp700.000) ⭐ **Harga Baru**
- Hot Stone Massage (Rp200.000)
- Aromatherapy Massage (Rp250.000)

### 3. **About**
- Informasi tentang layanan
- Stats: 5000+ Clients, 15 Therapists, 4.9★ Rating
- 10+ tahun pengalaman

### 4. **Booking**
- Dua pilihan terapis (Laki-laki / Perempuan)
- Direct WhatsApp booking link
- Touch-friendly buttons

### 5. **Contact**
- WhatsApp contact untuk perempuan dan laki-laki
- Jam operasional
- CTA card dengan gradient

### 6. **Footer**
- Quick links navigation
- Social media: Instagram, WhatsApp, TikTok
- Copyright information

---

## 🎨 Design System

### Color Palette
```css
Primary Green:    #7fb069
Light Green:      #a8d5a3
Dark Green:       #5a8c4f
Accent Green:     #b5e7a0
Background:       #f8fdf6
White:            #ffffff
Text Dark:        #2d3e2f
Text Gray:        #6b7c6e
```

### Typography
- **Headings:** Playfair Display (Serif)
- **Body:** Inter (Sans-serif)
- **Fluid Sizing:** clamp() untuk responsive scaling

### Spacing Scale (8px base)
```
xs:  8px    md:  16px   xl:  32px   3xl: 60px
sm:  12px   lg:  24px   2xl: 40px   4xl: 80px
```

### Breakpoints
```
Mobile:        320px - 480px
Mobile Large:  481px - 768px
Tablet:        768px - 1024px
Desktop:       1024px - 1440px
Large Desktop: 1440px+
```

---

## 🔧 Customization

### Mengubah Warna
Edit CSS variables di `style.css`:
```css
:root {
  --primary: #7fb069;        /* Warna utama */
  --primary-light: #a8d5a3;  /* Warna terang */
  --primary-dark: #5a8c4f;   /* Warna gelap */
}
```

### Menambah Layanan Baru
Di `index.html`, tambahkan card baru:
```html
<div class="card fade-in">
  <div class="card-icon">
    <i class="fa-solid fa-spa"></i>
  </div>
  <h3>Nama Layanan</h3>
  <p>Deskripsi layanan...</p>
  <div class="card-footer">
    <span class="price">Rp300.000</span>
    <span class="duration"><i class="fa-regular fa-clock"></i> 90 min</span>
  </div>
</div>
```

### Menambah Badge "Harga Baru"
Tambahkan class `price-updated` dan element badge:
```html
<div class="card fade-in price-updated">
  <div class="card-icon">
    <i class="fa-solid fa-spa"></i>
  </div>
  <div class="price-badge">Harga Baru</div>
  <!-- rest of card content -->
</div>
```

### Mengubah Kontak WhatsApp
Edit nomor di section booking dan contact:
```html
<a href="https://wa.me/628XXXXXXXXXX" target="_blank" class="btn-primary">
  <i class="fa-brands fa-whatsapp"></i> Book via WhatsApp
</a>
```

### Mengubah Social Media Links
Edit di footer section:
```html
<a href="https://www.instagram.com/your_username" target="_blank">
  <i class="fa-brands fa-instagram"></i>
</a>
```

---

## 📱 Responsive Design

Website ini 100% responsive dengan optimasi khusus untuk:

### Mobile (320px - 768px)
- ✅ Single column layout
- ✅ Hamburger menu navigation
- ✅ Touch-friendly buttons (min 44px)
- ✅ Stacked card footer
- ✅ Optimized falling leaves (8 leaves)
- ✅ Full-width CTA buttons

### Tablet (768px - 1024px)
- ✅ 2-column card grid
- ✅ Side-by-side about section
- ✅ Touch-optimized spacing
- ✅ Collapsible navigation

### Desktop (1024px+)
- ✅ 3-4 column card grid
- ✅ Fixed navbar with blur effect
- ✅ Hover effects on cards and buttons
- ✅ Optimal reading width (1200px max)

---

## ⚡ Performance

### Optimizations
- Pure HTML/CSS/JS (no frameworks = faster load)
- Minimal dependencies (only Font Awesome for icons)
- Optimized animations (GPU accelerated)
- Lazy-loaded falling leaves
- Reduced animation count on mobile

### Load Time
- First Contentful Paint: < 1s
- Time to Interactive: < 2s
- Total Page Size: < 500KB

---

## ♿ Accessibility

- ✅ **WCAG AAA Touch Targets** - All buttons minimum 44×44px
- ✅ **Color Contrast** - Meets WCAG AA standards
- ✅ **Semantic HTML** - Proper heading hierarchy
- ✅ **Aria Labels** - For better screen reader support
- ✅ **Keyboard Navigation** - Full keyboard accessibility
- ✅ **Focus States** - Visible focus indicators

---

## 🌙 Dark Mode

Website mendukung dark mode dengan:
- Toggle button di navbar
- Smooth transition animations
- Persisten (tersimpan di localStorage)
- Optimized colors untuk readability
- Adjusted shadows dan borders

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure & content |
| CSS3 | Styling & animations |
| JavaScript | Interactivity |
| Font Awesome 6.5.0 | Icons |
| Google Fonts | Typography (Playfair Display, Inter) |

---

## 📝 Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Android)

---

## 🐛 Known Issues

Tidak ada known issues saat ini. Website telah ditest di berbagai browser dan device.

---

## 🔄 Version History

### Version 2.0 (Current) - October 2026
- ✅ Complete UI/UX overhaul
- ✅ Enhanced responsive design
- ✅ Updated 4 service prices with visual highlights
- ✅ Standardized price format
- ✅ Improved typography system
- ✅ 8px-based spacing scale
- ✅ Enhanced dark mode
- ✅ Better accessibility (WCAG AAA)
- ✅ Optimized animations

### Version 1.0 - 2014
- Initial release
- Basic responsive design
- Dark mode feature
- 20 massage services

---

## 📞 Support

Untuk pertanyaan atau bantuan:
- 📱 WhatsApp (Perempuan): +62 878-4637-2118
- 📱 WhatsApp (Laki-laki): +62 898-9110-732
- 📧 Email: (add your email)
- 📍 Instagram: [@indahekawardani2808](https://www.instagram.com/indahekawardani2808)

---

## 📄 License

© 2026 Ummu Amirah Massage. All rights reserved.

---

## 🙏 Credits

- **Design & Development:** Revisi v2.0
- **Icons:** Font Awesome
- **Fonts:** Google Fonts (Playfair Display, Inter)
- **Original Concept:** Ummu Amirah Massage Team

---

## 📚 Documentation

Untuk dokumentasi lengkap tentang revisi terbaru, lihat:
- [REVISI_CHANGELOG.md](REVISI_CHANGELOG.md) - Detail semua perubahan

---

**Made with ❤️ for better user experience**
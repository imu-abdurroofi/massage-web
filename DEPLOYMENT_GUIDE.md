# 🚀 Deployment Guide - Ummu Amirah Massage Website

Panduan lengkap untuk deploy website ke **Vercel** (Recommended) atau platform lainnya.

---

## 📌 Table of Contents

1. [Deploy ke Vercel (Recommended)](#deploy-ke-vercel-recommended)
2. [Deploy ke Netlify](#deploy-ke-netlify)
3. [Deploy ke GitHub Pages](#deploy-ke-github-pages)
4. [Custom Domain Setup](#custom-domain-setup)
5. [Troubleshooting](#troubleshooting)

---

## 🎯 Deploy ke Vercel (Recommended)

### **Mengapa Vercel?**
- ⚡ Deploy super cepat (30 detik)
- 🌍 CDN global (website cepat di seluruh dunia)
- 🔄 Auto-deploy setiap push ke GitHub
- 📊 Built-in analytics gratis
- 🆓 100% gratis untuk project static

---

### **Metode 1: Via Vercel Dashboard** ⭐ **PALING MUDAH**

#### **Step 1: Buat Akun Vercel**
1. Buka [vercel.com](https://vercel.com)
2. Klik **"Sign Up"**
3. Pilih **"Continue with GitHub"**
4. Authorize Vercel untuk akses repository Anda

#### **Step 2: Import Project dari GitHub**
1. Di Vercel Dashboard, klik **"Add New..."** → **"Project"**
2. Klik **"Import Git Repository"**
3. Cari dan pilih repository **massage-web**
4. Klik **"Import"**

#### **Step 3: Configure Project Settings**

**Project Settings:**
```
Project Name:        ummu-amirah-massage
Framework Preset:    Other
Root Directory:      ./
Build Command:       (leave empty)
Output Directory:    (leave empty)
Install Command:     (leave empty)
```

**Environment Variables:** (tidak perlu untuk static site)

#### **Step 4: Deploy**
1. Klik tombol **"Deploy"**
2. Tunggu 30-60 detik
3. ✅ **Website LIVE!**

**URL Otomatis:**
```
https://ummu-amirah-massage.vercel.app
```

atau

```
https://massage-web-username.vercel.app
```

#### **Step 5: Setup Auto-Deploy**
✅ Sudah otomatis aktif!

Setiap kali Anda push ke GitHub:
- Branch `main` → Deploy ke Production
- Branch lain → Deploy ke Preview URL

---

### **Metode 2: Via Vercel CLI**

#### **Step 1: Install Vercel CLI**

**Windows (with npm):**
```bash
npm install -g vercel
```

**Windows (with download):**
- Download dari [vercel.com/download](https://vercel.com/download)
- Install seperti aplikasi biasa

#### **Step 2: Login ke Vercel**
```bash
cd c:\massage-web
vercel login
```

Browser akan terbuka untuk login dengan GitHub.

#### **Step 3: Deploy ke Preview**
```bash
vercel
```

Jawab pertanyaan:
```
? Set up and deploy? [Y/n] Y
? Which scope? (pilih account Anda)
? Link to existing project? [y/N] N
? What's your project's name? ummu-amirah-massage
? In which directory is your code located? ./
```

Akan deploy ke preview URL.

#### **Step 4: Deploy ke Production**
```bash
vercel --prod
```

✅ **Website live di production URL!**

#### **Command Berguna:**
```bash
vercel ls                 # List semua deployment
vercel inspect           # Inspect current deployment
vercel logs              # View deployment logs
vercel domains           # Manage domains
vercel env               # Manage environment variables
```

---

### **Vercel Configuration (vercel.json)**

File `vercel.json` sudah dibuat untuk optimasi:

```json
{
  "version": 2,
  "name": "ummu-amirah-massage",
  "builds": [...],
  "routes": [...],
  "headers": [...]
}
```

**Features:**
- ✅ Static file optimization
- ✅ Cache headers untuk performance
- ✅ HTML tidak di-cache (selalu fresh)
- ✅ Assets di-cache 1 tahun (CSS, JS, images)

---

## 🌐 Deploy ke Netlify

### **Metode 1: Via Netlify Dashboard**

#### **Step 1: Buat Akun**
1. Buka [netlify.com](https://netlify.com)
2. Sign up dengan GitHub

#### **Step 2: New Site from Git**
1. Klik **"Add new site"** → **"Import an existing project"**
2. Pilih **"GitHub"**
3. Pilih repository **massage-web**

#### **Step 3: Build Settings**
```
Branch to deploy:    main
Build command:       (leave empty)
Publish directory:   .
```

#### **Step 4: Deploy**
Klik **"Deploy site"**

**URL:** `https://random-name.netlify.app`

---

### **Metode 2: Via Drag & Drop**

1. Buka [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag folder `c:\massage-web` ke area upload
3. ✅ **Instant deploy!**

**Kekurangan:** Tidak ada auto-deploy dari GitHub

---

## 📄 Deploy ke GitHub Pages

### **Setup GitHub Pages**

#### **Method 1: Settings (Simple)**

1. Push code ke GitHub (sudah dilakukan)
2. Buka repository di GitHub
3. Go to **Settings** → **Pages**
4. Source: **Deploy from a branch**
5. Branch: **main** → **/ (root)**
6. Click **Save**
7. Tunggu 2-5 menit

**URL:** `https://username.github.io/massage-web`

#### **Method 2: GitHub Actions (Advanced)**

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

---

## 🌍 Custom Domain Setup

### **Setup Custom Domain di Vercel**

#### **Step 1: Beli Domain**
Beli domain dari:
- [Namecheap](https://namecheap.com) (Recommended)
- [GoDaddy](https://godaddy.com)
- [Niagahoster](https://niagahoster.co.id) (Indonesia)
- [Rumahweb](https://rumahweb.com) (Indonesia)

Contoh domain bagus:
- `ummuamirahmassage.com`
- `amirahspa.com`
- `amirahmassage.id`

#### **Step 2: Tambah Domain di Vercel**

1. Buka project di Vercel Dashboard
2. Go to **Settings** → **Domains**
3. Klik **"Add"**
4. Masukkan domain Anda: `ummuamirahmassage.com`
5. Klik **"Add"**

#### **Step 3: Update DNS di Registrar**

Vercel akan memberikan DNS records. Tambahkan ke domain registrar:

**A Record:**
```
Type:  A
Name:  @
Value: 76.76.21.21
```

**CNAME Record:**
```
Type:  CNAME
Name:  www
Value: cname.vercel-dns.com
```

#### **Step 4: Verify**

1. Kembali ke Vercel Dashboard
2. Klik **"Verify"**
3. Tunggu propagasi DNS (5 menit - 48 jam)
4. ✅ **Domain aktif dengan HTTPS otomatis!**

---

### **Setup Custom Domain di Netlify**

Sama seperti Vercel, tapi DNS records berbeda:

**A Record:**
```
Type:  A
Name:  @
Value: 75.2.60.5
```

**CNAME Record:**
```
Type:  CNAME
Name:  www
Value: apex-loadbalancer.netlify.com
```

---

## 🔧 Troubleshooting

### **1. Vercel Deploy Gagal**

**Problem:** Build failed atau error saat deploy

**Solution:**
```bash
# Check vercel.json syntax
cat vercel.json

# Remove vercel.json dan coba lagi
rm vercel.json
vercel --prod

# Check logs
vercel logs
```

### **2. Website Tidak Update**

**Problem:** Website masih tampil versi lama

**Solution:**
- **Clear browser cache:** Ctrl + Shift + R (hard refresh)
- **Check deployment:** Pastikan commit sudah di-push
- **Vercel:** Check dashboard, deployment status
- **Wait:** Propagasi bisa 1-5 menit

### **3. Custom Domain Tidak Jalan**

**Problem:** Domain tidak bisa diakses

**Solution:**
1. **Check DNS propagation:** [whatsmydns.net](https://whatsmydns.net)
2. **Verify DNS records:** Pastikan A/CNAME record benar
3. **Wait:** DNS propagasi bisa 24-48 jam
4. **Contact support:** Vercel/Netlify support sangat responsive

### **4. HTTPS/SSL Error**

**Problem:** "Not Secure" atau SSL error

**Solution:**
- **Vercel/Netlify:** HTTPS otomatis, tunggu 5-10 menit
- **Force HTTPS:** Enable di dashboard settings
- **Custom domain:** Tunggu DNS propagasi selesai

### **5. GitHub Pages 404**

**Problem:** Page not found setelah deploy

**Solution:**
1. Check **Settings → Pages** aktif
2. Branch harus **main** dan root **/**
3. Tunggu 2-5 menit build selesai
4. Check URL: `username.github.io/massage-web`

---

## 📊 Post-Deployment Checklist

### **After Deploy:**

- [ ] ✅ Website bisa diakses via URL
- [ ] ✅ Test di mobile dan desktop
- [ ] ✅ Test dark mode toggle
- [ ] ✅ Test hamburger menu
- [ ] ✅ Test semua link WhatsApp
- [ ] ✅ Test link Instagram, TikTok
- [ ] ✅ Verify 4 badge "Harga Baru" muncul
- [ ] ✅ Test smooth scroll navigation
- [ ] ✅ Test di berbagai browser (Chrome, Firefox, Safari)
- [ ] ✅ Check loading speed (< 2 detik)
- [ ] ✅ Setup analytics (Google Analytics atau Vercel Analytics)

---

## 📈 Setup Analytics

### **Vercel Analytics (Recommended)**

1. Buka project di Vercel Dashboard
2. Go to **Analytics** tab
3. Click **"Enable"**
4. ✅ Done! (Gratis 25k pageviews/bulan)

### **Google Analytics**

1. Buat account di [analytics.google.com](https://analytics.google.com)
2. Get tracking ID: `G-XXXXXXXXXX`
3. Tambahkan ke `index.html` sebelum `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🎯 Next Steps

### **Recommended Actions:**

1. **Setup Custom Domain** (opsional tapi professional)
   - Beli domain .com atau .id
   - Biaya: Rp100.000 - Rp200.000/tahun

2. **Enable Analytics** (penting untuk tracking)
   - Vercel Analytics (gratis, mudah)
   - atau Google Analytics

3. **Setup Social Media**
   - Instagram Business Account
   - Facebook Page
   - Google My Business

4. **SEO Optimization**
   - Submit to Google Search Console
   - Create sitemap.xml
   - Add meta descriptions

5. **Marketing**
   - Share link di Instagram Story
   - WhatsApp Status
   - Google Ads (optional)

---

## 💡 Tips & Best Practices

### **Deployment:**
- ✅ Selalu test di localhost dulu sebelum deploy
- ✅ Commit dengan pesan yang jelas
- ✅ Deploy ke preview dulu, baru production
- ✅ Backup sebelum perubahan besar

### **Performance:**
- ✅ Optimize gambar (compress sebelum upload)
- ✅ Minimize CSS/JS (jika site makin besar)
- ✅ Use CDN untuk assets

### **Security:**
- ✅ Selalu gunakan HTTPS
- ✅ Update dependencies reguler
- ✅ Jangan commit sensitive data (API keys, passwords)

### **Maintenance:**
- ✅ Monitor analytics weekly
- ✅ Test website di device berbeda
- ✅ Update harga/konten saat perlu
- ✅ Backup code reguler

---

## 📞 Support

### **Vercel Support:**
- Docs: [vercel.com/docs](https://vercel.com/docs)
- Discord: [vercel.com/discord](https://vercel.com/discord)
- Twitter: [@vercel](https://twitter.com/vercel)

### **Netlify Support:**
- Docs: [docs.netlify.com](https://docs.netlify.com)
- Forum: [answers.netlify.com](https://answers.netlify.com)

### **Domain Support:**
- Namecheap: Live chat 24/7
- Niagahoster: WhatsApp support

---

## 🎉 Congratulations!

Website Anda sudah siap online dan bisa diakses dari mana saja! 🚀

**Quick Links:**
- 🌐 Production URL: (akan muncul setelah deploy)
- 📊 Analytics: Vercel Dashboard
- ⚙️ Settings: Vercel Project Settings
- 📝 Docs: README.md

---

**Happy Deploying!** 🎊

*Last updated: Oktober 2026*

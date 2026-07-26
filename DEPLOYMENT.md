# Deployment Guide - Deçan Konnect

This document provides step-by-step instructions for deploying your Deçan Konnect website to various platforms.

---

## 1. Deploy to Vercel (Recommended) ⚡

**Pros:** Free tier, auto-deploys on push, fast CDN, built-in analytics
**Time:** 5 minutes

### Steps

1. **Push to GitHub** (if not already done):
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Go to [vercel.com](https://vercel.com)**

3. **Click "New Project"**

4. **Select your GitHub repository:**
   - Search for `Decan-konnect`
   - Click "Import"

5. **Configure project:**
   - Framework: `Other` (Static Site)
   - Build Command: Leave blank (or `echo 'Static site'`)
   - Output Directory: `.` (root)
   - Install Command: Leave blank

6. **Click "Deploy"** - Done! 🎉

### Your site is now live at:
```
https://decan-konnect.vercel.app
```

### Custom Domain (Optional)

1. In Vercel dashboard → Settings → Domains
2. Add your custom domain (e.g., `decan-konnect.com`)
3. Update DNS records at your domain provider
4. Wait 5-48 hours for DNS propagation

---

## 2. Deploy to GitHub Pages

**Pros:** Free, integrated with GitHub, no additional setup
**Time:** 3 minutes

### Steps

1. **Make sure your repo is public:**
   - Go to repo Settings → Danger Zone
   - Click "Make public" (if private)

2. **Push your code:**
   ```bash
   git push origin main
   ```

3. **Go to repo Settings → Pages**

4. **Configure:**
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
   - Click "Save"

5. **Wait 1-2 minutes** for deployment

### Your site is now live at:
```
https://lenvartica.github.io/Decan-konnect
```

---

## 3. Deploy to Netlify

**Pros:** Free tier, drag-and-drop deployment, form handling
**Time:** 5 minutes

### Method A: GitHub Integration

1. **Go to [netlify.com](https://netlify.com)**

2. **Click "New site from Git"**

3. **Connect GitHub account** and select your repo

4. **Configure:**
   - Build command: (leave blank)
   - Publish directory: `.`

5. **Click "Deploy"**

### Method B: Drag & Drop

1. **Go to [netlify.com](https://netlify.com)**

2. **Drag your project folder** into the upload area

3. **Wait for deployment** ✅

### Your site is now live at:
```
https://decan-konnect.netlify.app
```

---

## 4. Deploy to Cloudflare Pages

**Pros:** Fast CDN, free tier, excellent performance
**Time:** 5 minutes

### Steps

1. **Go to [pages.cloudflare.com](https://pages.cloudflare.com)**

2. **Click "Create a project" → "Connect to Git"**

3. **Select your GitHub repository**

4. **Configure:**
   - Framework: `None`
   - Build command: (leave blank)
   - Build output directory: `.`

5. **Click "Save and Deploy"**

### Your site is now live at:
```
https://decan-konnect.pages.dev
```

---

## 5. Deploy to Traditional Web Host

**Platforms:** Bluehost, GoDaddy, Hostinger, NameCheap, etc.
**Time:** 10-30 minutes

### Via FTP/SFTP

1. **Get FTP credentials** from your hosting control panel

2. **Download FTP client:**
   - FileZilla (free, cross-platform)
   - Cyberduck (Mac/Windows)
   - WinSCP (Windows)

3. **Connect to your server:**
   - Host: `ftp.yourdomain.com` or IP address
   - Username: Your FTP username
   - Password: Your FTP password
   - Port: 21 (FTP) or 22 (SFTP)

4. **Upload files:**
   - Navigate to `public_html/` or `www/` folder
   - Drag all project files there
   - Wait for upload to complete

5. **Visit your domain:**
   ```
   https://yourdomain.com
   ```

### Via cPanel File Manager

1. **Log into cPanel**

2. **Go to File Manager**

3. **Navigate to `public_html/`**

4. **Upload files:**
   - Use "Upload" button
   - Or drag files directly

5. **Visit your domain**

### Via SSH (Advanced)

```bash
# SSH into your server
ssh username@yourdomain.com

# Navigate to public folder
cd public_html/

# Clone repository
git clone https://github.com/lenvartica/Decan-konnect.git .

# Done!
```

---

## 6. Deploy to AWS S3 + CloudFront

**Pros:** Highly scalable, enterprise-grade, fast CDN
**Time:** 15 minutes

### Steps

1. **Create AWS S3 bucket:**
   - Go to [aws.amazon.com](https://aws.amazon.com)
   - Create S3 bucket named `decan-konnect`
   - Enable static website hosting

2. **Upload files:**
   ```bash
   aws s3 sync . s3://decan-konnect/
   ```

3. **Create CloudFront distribution:**
   - Point to S3 bucket
   - Set index.html as default root

4. **Get your CloudFront URL:**
   ```
   https://d123456.cloudfront.net
   ```

---

## Environment Variables

### For Netlify Forms

If using Netlify's form handling:

```html
<form name="contact" method="POST" netlify>
  <input type="text" name="name" required>
  <input type="email" name="email" required>
  <textarea name="message" required></textarea>
  <button type="submit">Send</button>
</form>
```

### For Formspree (No Backend)

1. **Go to [formspree.io](https://formspree.io)**
2. **Create free account**
3. **Get form endpoint**
4. **Update form action in HTML:**
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

---

## Domain Setup

### Map Custom Domain

#### For Vercel
1. Settings → Domains
2. Add domain
3. Update DNS at registrar to Vercel nameservers

#### For GitHub Pages
1. Settings → Pages → Custom domain
2. Enter domain
3. Update DNS CNAME record to `lenvartica.github.io`

#### For Netlify
1. Domain settings
2. Add custom domain
3. Update DNS CNAME/A records

#### For Traditional Host
1. Update nameservers to your host's
2. Or update A record to server IP
3. Wait 24-48 hours

---

## SSL/HTTPS Certificate

**All platforms above automatically provide HTTPS.**

No additional setup needed! Your site is secure by default.

---

## Monitoring & Analytics

### Vercel Analytics
- Dashboard shows page views, performance metrics
- Free tier included

### Google Analytics
1. Go to [analytics.google.com](https://analytics.google.com)
2. Create property
3. Get tracking code
4. Add to HTML head:
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'G-XXXXXXXXXX');
   </script>
   ```

### Cloudflare Analytics
- Automatic with Cloudflare Pages
- Shows traffic, threats, performance

---

## Auto-Deploy on Git Push

All modern platforms support auto-deploy:

```bash
# Just push to main branch
git add .
git commit -m "Update content"
git push origin main

# Site auto-updates in 1-2 minutes! ✨
```

---

## Troubleshooting

### Site shows 404
- Ensure `index.html` is in root directory
- Check build settings (should be empty for static site)
- Try clearing browser cache

### Forms not working
- Use Formspree or Netlify forms
- Check browser console for errors
- Verify form endpoint URL

### Slow performance
- Minify CSS/JS
- Compress images
- Use CDN (all platforms above do this)
- Check Lighthouse score

### DNS issues
- Wait 24-48 hours for propagation
- Verify DNS records are correct
- Use [whatsmydns.net](https://whatsmydns.net) to check

---

## Comparison Table

| Platform | Ease | Price | Performance | Auto-Deploy | Custom Domain |
|----------|------|-------|-------------|-------------|---------------|
| Vercel | ⭐⭐⭐⭐⭐ | Free | ⭐⭐⭐⭐⭐ | Yes | Yes |
| GitHub Pages | ⭐⭐⭐⭐⭐ | Free | ⭐⭐⭐⭐ | Yes | Yes |
| Netlify | ⭐⭐⭐⭐ | Free | ⭐⭐⭐⭐⭐ | Yes | Yes |
| Cloudflare Pages | ⭐⭐⭐⭐ | Free | ⭐⭐⭐⭐⭐ | Yes | Yes |
| Traditional Host | ⭐⭐⭐ | $3-15/mo | ⭐⭐⭐ | No | Yes |
| AWS S3 | ⭐⭐ | $0.024/GB | ⭐⭐⭐⭐⭐ | No | Yes |

---

**Questions? Contact us at contact@decan-konnect.com**

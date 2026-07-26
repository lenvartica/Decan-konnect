# Deçan Konnect - Technology Company Portfolio

**Building the Future Through Code, AI & Innovation**

Official website for Deçan Konnect, a Kenyan technology company founded by Lenny Muriuki. The site showcases our expertise in AI development, web design, mobile applications, and digital transformation services.

🌐 **Live Site:** [https://decan-konnect.vercel.app](https://decan-konnect.vercel.app)

---

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## ✨ Features

✅ **Fully Responsive** - Mobile, tablet, and desktop optimized
✅ **Dark Theme** - Modern dark UI with cyan accents
✅ **Smooth Animations** - Canvas particle effects, scroll animations, transitions
✅ **Interactive Elements** - FAQ accordions, smooth scroll navigation, form handling
✅ **SEO Optimized** - Meta tags, structured markup, fast load times
✅ **Cookie Consent** - GDPR-compliant cookie banner
✅ **Social Integration** - Links to GitHub, Instagram, Facebook, WhatsApp
✅ **Newsletter Signup** - Email subscription form
✅ **Contact Form** - Get in touch functionality
✅ **Fast Performance** - No build step, CDN-hosted assets

---

## 🛠️ Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Grid, Flexbox, animations, variables
- **JavaScript (Vanilla)** - No frameworks, pure DOM manipulation
- **Canvas API** - Particle animation effects
- **Font Awesome 6.4** - Icon library (CDN)
- **Google Fonts** - Inter & Poppins typefaces (CDN)
- **Vercel** - Deployment hosting

---

## 🚀 Getting Started

### Prerequisites
- Any modern web browser
- Optional: Node.js 16+ (for local development server)
- Optional: Git for version control

### Installation

#### Method 1: Direct Browser (Recommended for quick preview)

```bash
git clone https://github.com/lenvartica/Decan-konnect.git
cd Decan-konnect
open index.html
```

#### Method 2: Local Server (Python 3)

```bash
git clone https://github.com/lenvartica/Decan-konnect.git
cd Decan-konnect
python3 -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

#### Method 3: Local Server (Node.js)

```bash
git clone https://github.com/lenvartica/Decan-konnect.git
cd Decan-konnect
npx http-server
```

Then visit `http://localhost:8080` in your browser.

#### Method 4: Live Server (VS Code)

1. Install the "Live Server" extension in VS Code
2. Right-click `index.html` → Select "Open with Live Server"
3. Page auto-refreshes on save

---

## 📁 Project Structure

```
Decan-konnect/
├── index.html              # Main HTML file (all sections)
├── css/
│   ├── styles.css          # Main stylesheet
│   └── responsive.css      # Mobile & tablet breakpoints
├── js/
│   └── script.js           # Main JavaScript logic
├── assets/                 # Images, icons, favicon (not yet created)
│   ├── favicon.svg
│   ├── apple-touch-icon.png
│   ├── og-image.jpg
│   └── twitter-image.jpg
├── .github/
│   └── workflows/          # CI/CD workflows (empty)
├── .gitignore              # Git ignore rules
├── package.json            # Project metadata
├── README.md               # This file
└── decan-konnect.zip       # Archived version
```

---

## 🎨 Customization

### Colors & Theme

Edit `css/styles.css` root variables (lines 4–23):

```css
:root {
  --bg-primary: #0a0e27;     /* Main background */
  --accent: #00f2fe;         /* Highlight color */
  --primary: #4f46e5;        /* Button color */
  --whatsapp: #25d366;       /* WhatsApp button */
  /* ... more variables ... */
}
```

### Content Updates

1. **Replace text** in `index.html` (sections, descriptions, project details)
2. **Update links** (social, GitHub, WhatsApp group/channel)
3. **Add images** to `assets/` folder and reference them in HTML
4. **Modify contact email** (line 894)
5. **Update phone number** (line 901)

### Form Integration

To send contact form data:

1. Use a backend service like:
   - [Formspree](https://formspree.io/) (no backend needed)
   - [EmailJS](https://www.emailjs.com/) (client-side email)
   - [Firebase](https://firebase.google.com/) (database + email)
   - Your own Node.js API

2. Update form submission handler in `js/script.js` (lines 154–160)

---

## 🚢 Deployment

### Deploy to Vercel (Recommended)

1. Push code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project" → Select your repo
4. Click "Deploy"
5. Your site is live! (auto-updates on git push)

### Deploy to GitHub Pages

```bash
# Push to GitHub
git push origin main
```

Then in GitHub repo settings:
- Go to **Settings** → **Pages**
- Set source to `main` branch
- Your site is live at `https://lenvartica.github.io/Decan-konnect`

### Deploy to Netlify

1. Connect GitHub repo
2. Set build command: `echo "Static site - no build needed"`
3. Set publish directory: `.` (root)
4. Deploy

### Manual Deployment

Upload files to any web host (Bluehost, GoDaddy, Hostinger, etc.):

```bash
# Via FTP/SFTP
Upload all files to public_html/ or www/
```

---

## 📝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Make changes and test locally
4. Commit with clear messages (`git commit -m "Add: new feature"`)
5. Push to your fork (`git push origin feature/your-feature`)
6. Open a Pull Request

### Coding Standards

- Use semantic HTML5 tags
- Follow existing CSS naming (BEM-ish pattern)
- Add comments for complex JavaScript logic
- Test on mobile devices before committing
- Keep file sizes minimal (no large images or libraries)

---

## 📜 License

This project is licensed under the **MIT License** - see LICENSE file for details.

You are free to use, modify, and distribute this code for personal and commercial projects.

---

## 📞 Contact

**Deçan Konnect**

- 📧 Email: [contact@decan-konnect.com](mailto:contact@decan-konnect.com)
- 🌍 Website: [https://decan-konnect.vercel.app](https://decan-konnect.vercel.app)
- 💼 GitHub: [@lenvartica](https://github.com/lenvartica)
- 📱 WhatsApp: [Join Community](https://chat.whatsapp.com/II5OcY121lE7tQYSZHBVha)
- 📘 Facebook: [Lenny.Decan](https://www.facebook.com/Lenny.Decan.01)
- 📷 Instagram: [@its._.decan](https://www.instagram.com/its._.decan)

---

## 🙏 Acknowledgments

- Font Awesome for icons
- Google Fonts for typography
- Vercel for deployment
- All contributors and supporters

---

**Built with ❤️ by [Lenny Muriuki](https://github.com/lenvartica)**

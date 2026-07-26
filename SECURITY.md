# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in Deçan Konnect, please **do not** open a public GitHub issue.

Instead, please email us at: **lennymuriuki7@gmail.com** with:

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if you have one)

We will acknowledge your report within 48 hours and work on a fix.

---

## Security Best Practices

This project follows security best practices:

### Frontend Security
- ✅ No sensitive data stored in browser
- ✅ No API keys hardcoded
- ✅ HTTPS enforced on all deployments
- ✅ Content Security Policy headers recommended
- ✅ XSS protection (no eval, no innerHTML for user input)
- ✅ CSRF protection via form tokens (when using backend)

### Form Security
- ✅ Client-side validation
- ✅ Server-side validation required (implement when adding backend)
- ✅ Rate limiting recommended
- ✅ CAPTCHA recommended for contact form

### Dependency Security
- ✅ No npm dependencies (static site)
- ✅ All CDN dependencies from official sources:
  - Font Awesome: cdnjs.cloudflare.com
  - Google Fonts: fonts.googleapis.com
  - HTTP only (browser auto-upgrades to HTTPS)

### Deployment Security
- ✅ HTTPS/SSL enforced
- ✅ Security headers set by platform
- ✅ DDoS protection via CDN
- ✅ Automatic security updates

---

## Infrastructure Security

When deploying, ensure:

1. **Enable HTTPS** - All platforms above provide this
2. **Set Security Headers:**
   ```
   X-Content-Type-Options: nosniff
   X-Frame-Options: SAMEORIGIN
   X-XSS-Protection: 1; mode=block
   Referrer-Policy: strict-origin-when-cross-origin
   ```
3. **Content Security Policy:**
   ```
   default-src 'self';
   script-src 'self' cdnjs.cloudflare.com;
   style-src 'self' fonts.googleapis.com cdnjs.cloudflare.com;
   font-src fonts.gstatic.com cdnjs.cloudflare.com;
   ```

---

## Data Privacy

### What We Don't Collect
- ❌ We don't track personal data without consent
- ❌ We don't store form submissions without explicit backend
- ❌ We don't use analytics by default (optional via Google Analytics)

### Cookie Consent
- ✅ Cookie banner shown to users
- ✅ User choice respected
- ✅ No cookies set without consent

### When Adding Backend Services

If you add form handling or analytics:
1. Update Privacy Policy
2. Get explicit user consent
3. Comply with GDPR, CCPA, etc.
4. Use encrypted connections (HTTPS)
5. Secure data storage

---

## Contributing Securely

If you're contributing:

1. **Don't commit secrets:**
   - No API keys
   - No passwords
   - No private tokens

2. **Use .gitignore:**
   ```
   .env
   .env.local
   secrets.json
   ```

3. **Review before push:**
   ```bash
   git diff --cached
   ```

4. **If you accidentally commit secrets:**
   ```bash
   git reset HEAD~1  # Undo commit
   echo "secrets.json" >> .gitignore
   git add .gitignore
   git commit -m "Remove secrets"
   ```

---

## Third-Party Services

When adding integrations:

- ✅ Use official libraries
- ✅ Keep libraries updated
- ✅ Review terms of service
- ✅ Understand privacy implications
- ✅ Use HTTPS endpoints only

### Safe Services for This Project

- **Forms:** Formspree, Netlify Forms, Basin, 99inbound
- **Analytics:** Google Analytics, Plausible, Fathom
- **Email:** EmailJS, Nodemailer (if self-hosted)
- **Hosting:** Vercel, Netlify, GitHub Pages, Cloudflare
- **CDN:** Cloudflare, jsDelivr, cdnjs, unpkg

---

## Vulnerability Disclosure Timeline

- **Immediate:** Acknowledge receipt
- **24-48 hours:** Preliminary investigation
- **3-7 days:** Fix development
- **1-2 days:** Testing and verification
- **Release:** Public announcement with fix and credits

---

## Security Headers Example

For Vercel (`vercel.json`):
```json
{
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "SAMEORIGIN"
        },
        {
          "key": "X-XSS-Protection",
          "value": "1; mode=block"
        },
        {
          "key": "Referrer-Policy",
          "value": "strict-origin-when-cross-origin"
        }
      ]
    }
  ]
}
```

---

## Questions?

📧 Email: contact@decan-konnect.com
🔗 GitHub: https://github.com/lenvartica/Decan-konnect

---

**Security is everyone's responsibility. Thank you for helping keep Deçan Konnect secure!**

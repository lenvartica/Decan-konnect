# Contributing to Deçan Konnect

Thank you for your interest in contributing to Deçan Konnect! This document provides guidelines and instructions for contributing.

## Code of Conduct

- Be respectful and inclusive
- Provide constructive feedback
- Accept criticism gracefully
- Focus on the code, not the person

## Getting Started

1. **Fork** the repository on GitHub
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/Decan-konnect.git
   cd Decan-konnect
   ```
3. **Create a feature branch:**
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Making Changes

### HTML
- Use semantic HTML5 tags (`<header>`, `<nav>`, `<section>`, `<article>`, etc.)
- Maintain proper heading hierarchy (h1 → h2 → h3)
- Add alt text to all images
- Validate with W3C validator

### CSS
- Follow existing naming conventions (loose BEM pattern)
- Use CSS custom properties (variables) for colors and sizes
- Mobile-first approach: styles start at mobile, media queries add for larger screens
- Keep specificity low, avoid `!important`
- Add comments for complex rules

### JavaScript
- Use `const`/`let`, avoid `var`
- Add null checks before DOM manipulation
- Keep functions small and focused (single responsibility)
- Add comments explaining non-obvious logic
- Use meaningful variable names
- No console.log() in production code

### General
- Keep files under 20KB where possible
- Minimize external dependencies
- Test on mobile devices (use DevTools)
- Check performance: DevTools → Lighthouse

## Testing

### Before Submitting

1. **Test locally:**
   ```bash
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000`

2. **Test on multiple devices:**
   - Desktop (Chrome, Firefox, Safari, Edge)
   - Tablet (iPad, Android tablet)
   - Mobile (iPhone, Android phone)

3. **Use browser DevTools:**
   - Responsive design mode
   - Lighthouse audit
   - Console for errors
   - Network tab for performance

4. **Check accessibility:**
   - Keyboard navigation (Tab key)
   - Screen reader compatibility (VoiceOver, NVDA)
   - Color contrast (Chrome DevTools)

## Commit Guidelines

### Format
```
<type>: <subject>

<body (optional)>

<footer (optional)>
```

### Types
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` CSS/formatting changes
- `refactor:` Code restructuring
- `perf:` Performance improvements
- `test:` Test additions/updates
- `chore:` Build, dependencies, etc.

### Examples
```bash
git commit -m "feat: Add dark mode toggle"
git commit -m "fix: Hero canvas animation lag on mobile"
git commit -m "docs: Update README with deployment steps"
git commit -m "style: Adjust button hover colors"
```

## Pull Request Process

1. **Push to your fork:**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Open a Pull Request** on GitHub with:
   - Clear title describing the change
   - Description of what and why
   - Related issues (if any) - use `Fixes #123`
   - Screenshots if UI changes
   - Checklist:
     - [ ] Code follows project style
     - [ ] Changes tested locally
     - [ ] Works on mobile
     - [ ] No console errors
     - [ ] Comments added for complex logic

3. **Respond to review comments** within 48 hours

4. **Merge** - Project maintainers will merge after approval

## Common Contributions

### Adding a New Section

1. Add HTML structure in `index.html`
2. Add CSS in `css/styles.css` with descriptive comments
3. Add responsive styles in `css/responsive.css`
4. Add JavaScript functionality in `js/script.js` if needed
5. Add navigation link in navbar
6. Test on all devices

### Fixing a Bug

1. Create an issue describing the bug (if not already created)
2. Create a branch: `git checkout -b fix/bug-description`
3. Make minimal changes to fix only that bug
4. Test thoroughly
5. Commit and push
6. Reference the issue in your PR

### Improving Documentation

1. Update relevant `.md` files
2. Add examples if applicable
3. Check formatting with Markdown viewer
4. Submit PR

## Performance Guidelines

- Minimize CSS file sizes (concatenate if needed)
- Use efficient selectors (avoid deep nesting)
- Lazy load images (when feature is added)
- Minify JavaScript in production
- Cache assets appropriately
- Target Lighthouse score 90+

## Questions?

- Check existing issues/discussions
- Ask in pull request comments
- Email: contact@decan-konnect.com
- Join our WhatsApp community

---

**Thank you for contributing to Deçan Konnect! 🚀**

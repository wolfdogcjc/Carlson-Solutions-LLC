# Asset Management

This page defines guidelines for naming conventions, image optimization, and asset organization within the repository.

---

## Directory Structure

All static assets are stored in the `/assets/` directory at the repository root:

```
assets/
├── logo.svg                # Company logo — primary brand mark (SVG)
├── favicon.png             # Browser tab icon (PNG, 32×32px recommended)
├── data-protection.pdf     # Data Protection Policy
├── privacy-policy.pdf      # Privacy Policy
└── terms-of-service.pdf    # Terms of Service
```

---

## File Naming Conventions

| Rule | Good Example | Bad Example |
|---|---|---|
| Lowercase only | `hero-image.webp` | `Hero-Image.webp` |
| Hyphens as word separators (no spaces, no underscores) | `service-card-bg.webp` | `service card bg.webp`, `service_card_bg.webp` |
| Descriptive, purpose-driven names | `team-photo-2025.jpg` | `IMG_4821.jpg` |
| Include dimensions for multiple size variants | `logo-dark-256.png` | `logo-dark-large.png` |
| Format suffix matches actual format | `icon.svg` | `icon.svg.png` |

### PDF Documents

Legal and policy PDF documents should follow the pattern: `{document-type}.pdf`

Examples:
- `privacy-policy.pdf`
- `terms-of-service.pdf`
- `data-protection.pdf`

---

## Image Formats

| Format | When to Use |
|---|---|
| **SVG** | Logos, icons, illustrations — anything that needs to scale infinitely |
| **WebP** | Photos, hero images, team photos (smaller file size than JPEG/PNG) |
| **PNG** | Images requiring transparency that can't be SVG; favicon |
| **JPEG** | Legacy photo support only; prefer WebP for new images |
| **PDF** | Documents intended for download (policies, reports) |

> **Avoid GIF** — use CSS animations or short WebP animations instead.

---

## Image Optimization Guidelines

Before committing any image asset to the repository:

1. **Resize to the largest display size needed.** Avoid uploading 4K images if the maximum display width is 1200px.
2. **Compress images** using a tool such as:
   - [Squoosh](https://squoosh.app/) (browser-based, free)
   - [ImageOptim](https://imageoptim.com/) (macOS)
   - `cwebp` CLI for WebP conversion
3. **Target file sizes:**
   - Hero/banner images: < 200 KB
   - Card/thumbnail images: < 50 KB
   - Icons/logos: < 10 KB (SVG preferred)
   - Favicons: < 5 KB
4. **Always include `alt` text** on every `<img>` tag in `index.html` for accessibility and SEO.

---

## Adding a New Asset

1. Optimize the file following the guidelines above.
2. Name it according to the naming conventions.
3. Place it in the `/assets/` directory.
4. Reference it in `index.html` using the absolute path `/assets/filename.ext` to ensure compatibility with the local server and GitHub Pages.
5. Commit the asset alongside the HTML change that references it in the same commit.

### Example

```html
<!-- Correct: absolute path from repo root -->
<img src="/assets/team-photo-2025.webp" alt="Carlson Solutions team at a client site in 2025">

<!-- Avoid: relative paths that may break depending on serve context -->
<img src="assets/team-photo-2025.webp" alt="...">
```

---

## Asset Checklist Before Committing

- [ ] File name is lowercase with hyphens
- [ ] Image is resized to the appropriate dimensions
- [ ] Image is compressed to the target file size
- [ ] SVG is used where applicable instead of raster formats
- [ ] `alt` text is present on all `<img>` tags referencing the new asset
- [ ] The asset does not contain sensitive or confidential information
- [ ] No client data or PII is embedded in PDFs before publishing

---

## Updating Legal Documents (PDFs)

When updating `privacy-policy.pdf`, `terms-of-service.pdf`, or `data-protection.pdf`:

1. Review the document to ensure no confidential business or client data is included.
2. Replace the existing file in `/assets/` with the updated version using the **same filename** to avoid broken links.
3. Notify the site owner so the live site can be verified after deployment.

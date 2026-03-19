# Brand Guidelines

This page defines the visual identity standards for Carlson Solutions LLC to ensure UI consistency across the website and any future marketing materials.

---

## Color Palette

### Primary Colors

| Name | Hex | RGB | CSS Variable | Usage |
|---|---|---|---|---|
| **Cyan Accent** | `#22D3EE` | `34, 211, 238` | `--cyan-accent` | Primary CTAs, links, highlights, active nav states |
| **Cyan Hover** | `#67E8F9` | `103, 232, 249` | — | Button hover state (slightly lighter cyan) |
| **Near-Black** | `#09090B` | `9, 9, 11` | `--var-bg` | Dark mode page background |
| **Surface** | `rgba(24,24,27,0.6)` | `24,24,27 @ 60%` | `--var-card` | Dark mode card/panel backgrounds |

### Dark Mode

| Name | Value | CSS Variable | Usage |
|---|---|---|---|
| Border | `rgba(39,39,42,0.5)` | `--var-border` | Subtle card and divider borders |
| Primary Text | `#FFFFFF` | `--var-main` | All primary text and headings |
| Secondary Text | `#A1A1AA` | `--var-dim` | Subheadings, meta text, labels |
| Text (Buttons) | `#FFFFFF` | `--var-text-main` | Filled button label text |

### Light Mode

| Name | Value | CSS Variable | Usage |
|---|---|---|---|
| Background | `#FFFFFF` | `--var-bg` | Page background |
| Surface | `#F8FAFC` | `--var-card` | Card backgrounds |
| Border | `#CBD5E1` | `--var-border` | Card and divider borders |
| Primary Text | `#0F172A` | `--var-main` | All primary text and headings |
| Secondary Text | `#334155` | `--var-dim` | Subheadings, meta text, labels |
| Text (Buttons) | `#020617` | `--var-text-main` | Filled button label text |

---

## Typography

### Font Families

| Role | Font Family | Weights Used | CDN Source |
|---|---|---|---|
| **Headings** | Space Grotesk | 500, 600, 700 | Google Fonts |
| **Body / UI** | Inter | 400, 500, 600, 700, 900 | Google Fonts |

### Type Scale Guidelines

- **H1 (Hero):** `text-6xl` → `text-8xl` (responsive), `font-bold`, `tracking-tighter`
- **H2 (Section):** `text-3xl` → `text-4xl`, `font-bold`
- **H3 (Card):** `text-xl`, `font-bold`
- **Body:** `text-lg` → `text-xl` for descriptive paragraphs, `leading-relaxed`
- **Labels/Tags:** `text-xs`, `font-bold`, `uppercase`, `tracking-widest`

### CSS Class Application

Apply `class="heading-font"` to any element that should use Space Grotesk. All other text defaults to Inter via the `body` rule in `stylesheet.css`.

---

## Logo

### Primary Logo

- **File:** `assets/logo.svg`
- **Format:** SVG (scalable, preferred for all digital uses)
- **Default display size:** `w-10 h-10` (40×40px) in the navigation header
- **Behavior:** Rotates 12° on hover (`group-hover:rotate-12`) for a subtle interactive effect

### Usage Rules

- Always use the SVG version for web — never rasterize the logo at small sizes
- Maintain clear space equal to the logo's height on all sides when placing it in layouts
- Do not recolor, stretch, or add effects to the logo without approval
- On dark backgrounds, use the default SVG; on light backgrounds, verify contrast is sufficient

### Favicon

- **File:** `assets/favicon.png`
- **Format:** PNG
- **Usage:** Browser tab icon only (`<link rel="icon">`)

---

## UI Component Conventions

### Buttons

| Type | Classes | Use Case |
|---|---|---|
| Primary (filled) | `px-8 py-4 bg-cyan-400 hover:bg-cyan-300 text-zinc-950 rounded-full font-bold uppercase tracking-widest text-xs` | Primary CTAs (View Services, Get Quote) |
| Secondary (outline) | `px-8 py-4 bg-var-card text-var-main border border-var-border rounded-full font-bold uppercase tracking-widest text-xs hover:border-zinc-500` | Secondary actions |
| Nav CTA | `px-6 py-2.5 bg-var-text-main text-var-bg rounded-full font-bold text-xs uppercase tracking-widest hover:bg-cyan-400` | Header navigation CTA |

### Cards (Service Cards)

Service cards use a consistent structure:
- Background: `bg-var-card`
- Border: `border border-var-border`
- Rounded corners: `rounded-2xl` or `rounded-3xl`
- Padding: `p-8`
- Hover: subtle border highlight or lift effect

### Skill Bubbles

Small tag-like labels inside service cards. Applied with the `skill-bubble` CSS class defined in `stylesheet.css`. Used for technology/keyword labels (e.g., "UniFi", "Networking", "Audit").

### Accent Glow Effect

Cyan glow is applied using Tailwind's shadow utilities:
```
shadow-[0_0_20px_rgba(34,211,238,0.2)]
```
Use sparingly on primary CTA buttons and hero elements.

---

## Iconography

All icons are sourced from **Font Awesome 6 Free** (Solid style, `fas` class prefix).

| Icon | Class | Context |
|---|---|---|
| IT Management | `fa-laptop-code` | Service card |
| Security | `fa-shield-halved` | Service card / hero |
| Energy | `fa-bolt` | Service card / hero |
| UniFi Protect | `fa-camera` | Service card |
| Theme toggle (sun) | `fa-sun` | Light/dark toggle button |
| Theme toggle (moon) | `fa-moon` | Light/dark toggle button |
| External arrow | `fa-arrow-right` | CTA buttons |
| Hamburger menu | `fa-bars` | Mobile nav trigger |
| Close menu | `fa-xmark` | Mobile menu close |

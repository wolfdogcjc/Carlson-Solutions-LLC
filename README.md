# Carlson Solutions LLC

[![GitHub Pages](https://img.shields.io/badge/Deployed%20on-GitHub%20Pages-blue?logo=github)](https://wolfdogcjc.github.io/Carlson-Solutions-LLC/)

> Expert IT management, security consulting, and energy auditing for homes and businesses — serving Chisago County and beyond.

---

## 📋 Project Overview

**Carlson Solutions LLC** is a technology and consulting firm specializing in the following service areas:

| Service | Description |
|---|---|
| **IT Management** | UniFi network provisioning, server administration, and infrastructure consulting |
| **Security Consulting** | Physical security audits covering door hardware, access control, and circuit security |
| **Energy Auditing** | Building envelope and electrical system assessments to optimize efficiency |
| **Office Tech Setup** | Workstation and peripheral integration for local business or home office environments |
| **UniFi Protect Setup** | Camera and NVR configuration with recording logic, detection zones, and remote access |
| **Custom Project Requests** | Scoped and delivered technical solutions tailored to specific infrastructure needs |

This repository contains the source code for the public-facing company website, built as a single-page application (SPA) deployed via GitHub Pages.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Markup** | HTML5 |
| **Styling** | CSS3, [Tailwind CSS](https://tailwindcss.com/) (CDN) |
| **Icons** | [Font Awesome 6](https://fontawesome.com/) (CDN) |
| **Fonts** | [Inter](https://fonts.google.com/specimen/Inter) + [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (Google Fonts) |
| **Scripting** | Vanilla JavaScript (inline) |
| **Hosting** | GitHub Pages |
| **Assets** | SVG logo, PNG favicon, PDF legal documents |

> **No build tools or package managers are required.** The site runs entirely from static files with all dependencies loaded via CDN.

---

## 🚀 Installation & Local Setup

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- [Git](https://git-scm.com/) installed locally
- A static file server (optional, but recommended to avoid asset path issues)

### Steps

**1. Clone the repository**
```bash
git clone https://github.com/wolfdogcjc/Carlson-Solutions-LLC.git
cd Carlson-Solutions-LLC
```

**2. Serve the site locally**

Using Python's built-in HTTP server (recommended):
```bash
# Python 3
python -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080) in your browser.

Alternatively, using Node.js `serve`:
```bash
npx serve .
```

Or using VS Code's [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension — right-click `index.html` → **Open with Live Server**.

> **Note:** Opening `index.html` directly as a `file://` URL may cause some asset paths (e.g., `/assets/logo.svg`) to not resolve correctly. Always use a local server.

---

## 📁 Directory Structure

```
Carlson-Solutions-LLC/
├── index.html          # Main single-page website
├── 404.html            # Custom 404 error page
├── stylesheet.css      # Custom CSS variables, animations, and overrides
├── robots.txt          # Search engine crawl directives
├── sitemap.xml         # XML sitemap for SEO
├── assets/
│   ├── logo.svg        # Company logo (SVG, primary brand mark)
│   ├── favicon.png     # Browser tab icon (PNG)
│   ├── data-protection.pdf   # Data Protection Policy document
│   ├── privacy-policy.pdf    # Privacy Policy document
│   └── terms-of-service.pdf  # Terms of Service document
├── api/
│   └── send-quote.js   # Serverless function for quote form handling
├── docs/
│   └── wiki/           # Extended technical documentation
├── README.md           # This file
└── SECURITY.md         # Vulnerability reporting and security policy
```

---

## 🎨 Brand Colors

| Token | Hex | Usage |
|---|---|---|
| Cyan Accent | `#22D3EE` | Primary CTAs, highlights, active states |
| Background (Dark) | `#09090B` | Dark mode page background |
| Background (Light) | `#F8FBFF` | Light mode page background |
| Surface (Dark) | `rgba(24,24,27,0.6)` | Card and panel backgrounds (dark) |
| Surface (Light) | `#FFFFFF` | Card and panel backgrounds (light) |
| Body Text (Dark) | `#FFFFFF` | Primary text in dark mode |
| Muted Text (Dark) | `#A1A1AA` | Secondary/supporting text in dark mode |
| Body Text (Light) | `#0B1220` | Primary text in light mode |
| Muted Text (Light) | `#334155` | Secondary/supporting text in light mode |

Primary font: **Space Grotesk** (headings) / **Inter** (body)

---

## 📬 Contact

| Channel | Details |
|---|---|
| **Email** | [contact@carlsonsolutionsmn.com](mailto:contact@carlsonsolutionsmn.com) |
| **Phone** | [(651) 348-0615](tel:+16513480615) |
| **Website** | [carlsonsolutionsmn.com](https://carlsonsolutionsmn.com) |
| **LinkedIn** | [Carlson Solutions MN](https://www.linkedin.com/company/carlson-solutions-mn/) |
| **Facebook** | [Carlson Solutions LLC](https://www.facebook.com/p/Carlson-Solutions-LLC-61576075333873/) |
| **Google Reviews** | [Leave a Review](https://g.page/r/CW0czeTI0oIyEAE/review) |

For **security vulnerabilities**, please see [`SECURITY.md`](SECURITY.md) for responsible disclosure instructions — do **not** open a public GitHub issue.

---

## 📄 License

© Carlson Solutions LLC. All rights reserved. Unauthorized copying, distribution, or modification of this codebase is prohibited without express written consent.

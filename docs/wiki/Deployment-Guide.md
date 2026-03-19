# Deployment Guide

This page documents how the Carlson Solutions LLC website is hosted, deployed, and maintained.

---

## Hosting Provider

The website is hosted on **GitHub Pages** — GitHub's free static site hosting service. The site is served directly from the `main` branch of the repository.

- **Live URL:** `https://wolfdogcjc.github.io/Carlson-Solutions-LLC/` (or a custom domain if configured)
- **Source branch:** `main`
- **Publish directory:** Repository root (`/`)
- **Build process:** None — the site is pure static HTML/CSS/JS with no build step required

---

## Deployment Workflow

GitHub Pages automatically deploys the site whenever changes are pushed to the `main` branch. There is no manual deployment step required.

```
Developer → git push origin main → GitHub Pages builds → Site is live (within ~1 minute)
```

### Steps to deploy a change

1. Make your changes locally (see [README setup instructions](../README.md))
2. Test the site using a local server (`python -m http.server 8080`)
3. Commit your changes:
   ```bash
   git add .
   git commit -m "describe your change"
   git push origin main
   ```
4. Navigate to the live URL to verify the deployment (allow ~60 seconds for propagation)

---

## Custom Domain (If Applicable)

If a custom domain (e.g., `carlsonsolutionsmn.com`) is configured:

1. A `CNAME` file must exist at the repository root containing the domain name
2. DNS records must be set at the domain registrar:
   - `A` records pointing to GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a `CNAME` record pointing to `wolfdogcjc.github.io`
3. HTTPS is enforced automatically by GitHub Pages via Let's Encrypt

---

## CI/CD Pipeline

Currently, there is **no automated CI/CD pipeline** beyond GitHub Pages auto-deployment. Future improvements could include:

| Enhancement | Tool | Purpose |
|---|---|---|
| HTML validation | [html-validate](https://html-validate.org/) | Catch markup errors before deployment |
| Link checking | [lychee](https://github.com/lycheeverse/lychee) | Detect broken internal/external links |
| Accessibility audit | [axe](https://www.deque.com/axe/) | Ensure WCAG compliance |
| Performance audit | Lighthouse CI | Track Core Web Vitals over time |

---

## Rollback Procedure

Since every commit to `main` is tracked by Git, rolling back to a previous version is straightforward:

```bash
# Find the commit you want to revert to
git log --oneline

# Option 1: Revert the last commit (creates a new commit)
git revert HEAD

# Option 2: Hard reset to a specific commit (use with caution)
git reset --hard <commit-sha>
git push --force origin main
```

> ⚠️ **Use `--force` push sparingly** — it rewrites history and can cause issues for any collaborators.

# Security Policy

## Reporting a Vulnerability

**Please do NOT open a public GitHub issue to report a security vulnerability.**

If you discover a security vulnerability in the Carlson Solutions LLC website or codebase, we ask that you report it responsibly through our private disclosure process:

1. **Email us directly:** [contact@carlsonsolutionsmn.com](mailto:contact@carlsonsolutionsmn.com)
2. Use the subject line: `[SECURITY] Vulnerability Report`
3. Include the following details in your report:
   - A clear description of the vulnerability
   - Steps to reproduce the issue
   - Potential impact and severity assessment
   - Any suggested remediation (optional)

We will acknowledge receipt of your report within **48 hours** and aim to provide a resolution timeline within **7 business days**. We appreciate responsible disclosure and will credit researchers who follow this process (unless anonymity is preferred).

---

## Supported Versions

This project is a static website with continuous deployment. Only the latest version deployed on the `main` branch is actively maintained and receives security updates.

| Version | Status |
|---|---|
| `main` branch (latest) | ✅ Actively maintained |
| Previous deployments | ❌ No longer supported |

---

## Dependency Scanning

All third-party dependencies are loaded via CDN and are not bundled in this repository. To keep them current:

- **Tailwind CSS** — Update the CDN script tag in `index.html` to the latest stable version when a new major release is available.
- **Font Awesome** — Update the CDN link in `index.html` to the latest stable version periodically.
- **Google Fonts** — Font loading URLs should be reviewed if Google Fonts changes their API.

Periodically audit CDN-loaded libraries against known CVEs using resources such as:
- [Snyk Vulnerability Database](https://snyk.io/vuln/)
- [GitHub Advisory Database](https://github.com/advisories)
- [NIST NVD](https://nvd.nist.gov/)

---

## Secrets Management

This repository is a **public static site**. The following rules are strictly enforced:

- ❌ **Never** commit API keys, tokens, or credentials to this repository.
- ❌ **Never** commit client data, personally identifiable information (PII), or sensitive business data.
- ❌ **Never** commit environment variables (`.env` files) or configuration files containing secrets.
- ✅ All contact form submissions are handled client-side and must route through a secure, server-side backend or third-party form service — never inline credentials in JavaScript.
- ✅ PDF documents in the `assets/` folder (privacy policy, terms of service) must be reviewed before publishing to ensure no sensitive internal data is included.

If you suspect a secret has been accidentally committed to this repository, please report it immediately via the email above and treat the exposed credential as **compromised** — rotate it immediately regardless of whether the commit has been removed.

---

## Content Security

- The website does not collect or store user data directly.
- Any contact form integrations must use HTTPS endpoints exclusively.
- Third-party scripts (CDN resources) should be reviewed when updating to ensure they have not been compromised (supply chain integrity).

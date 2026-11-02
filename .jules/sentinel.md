## 2024-11-02 - Added Strict Content Security Policy (CSP)
**Vulnerability:** The static pages lacked a Content Security Policy, which could theoretically allow Cross-Site Scripting (XSS) if any dynamic content was later introduced or injected.
**Learning:** The project is entirely static HTML with inline CSS and no JavaScript or external assets. This allows for an extremely restrictive and secure CSP (`default-src 'none'; style-src 'unsafe-inline';`).
**Prevention:** Ensured that a strict CSP meta tag is present on all HTML pages to enforce defense-in-depth against unauthorized resource loading and execution.

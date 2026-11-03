## 2024-05-16 - Add strict Content Security Policy for static pages
**Vulnerability:** The static HTML pages lacked a Content Security Policy (CSP), which left them potentially vulnerable to Cross-Site Scripting (XSS) if user input or third-party content were later introduced.
**Learning:** For purely static sites with inline styles, it's possible to use a strict CSP without resorting to `'unsafe-inline'` by computing the SHA-256 hash of the inline CSS and including it in the `style-src` directive. This project requires this strict pattern.
**Prevention:** Always ensure any newly added static pages or modifications to inline CSS include or update the corresponding SHA-256 hash in the CSP `<meta>` tag.

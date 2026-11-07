## 2026-11-07 - Strict Content Security Policy for Static Sites
**Vulnerability:** The static HTML pages lack Content Security Policy (CSP) headers or meta tags, which violates defense-in-depth principles against potential injection or XSS, even on completely static sites.
**Learning:** For purely static HTML files without a web server to send HTTP headers, CSP can be enforced using `<meta http-equiv="Content-Security-Policy">` tags. It is possible to avoid `'unsafe-inline'` by calculating the SHA-256 hash of the inline `<style>` blocks and allowing those hashes explicitly.
**Prevention:** Always implement a strict default CSP (`default-src 'none'`) and selectively allow required resources, utilizing hashes for inline scripts and styles on static sites to avoid `'unsafe-inline'`.

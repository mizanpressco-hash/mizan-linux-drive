## 2024-10-31 - Strict CSP for Static Sites
**Vulnerability:** Missing Content Security Policy (CSP) headers in static HTML pages.
**Learning:** Even simple, purely static sites (no JS, no external assets) should have a strict CSP to prevent malicious injection via unexpected entry points or web hosting misconfigurations.
**Prevention:** Implement a strict CSP `<meta>` tag (e.g., `default-src 'none'; style-src 'unsafe-inline'; form-action 'none'; base-uri 'none';`) in the `<head>` of all static HTML files.

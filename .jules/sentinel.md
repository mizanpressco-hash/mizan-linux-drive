## 2024-05-25 - CSP Headers Missing
**Vulnerability:** Missing Content Security Policy (CSP) headers on static HTML pages.
**Learning:** Static HTML pages without a build system still need CSP headers to mitigate XSS and restrict resources, especially to enforce strict `style-src` hashes instead of `unsafe-inline` and block external scripts/assets.
**Prevention:** Always include `<meta http-equiv="Content-Security-Policy">` with strict directives (e.g., `default-src 'none'`, hashed `style-src`) in the `<head>` of all static HTML files.

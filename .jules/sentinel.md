## 2024-05-15 - Strict CSPs for Static HTML
**Vulnerability:** Static HTML pages lacked Content Security Policy (CSP) headers, making them potentially vulnerable to XSS or unwanted asset injection.
**Learning:** This project consists of purely static HTML files with inline CSS and no build system.
**Prevention:** Apply a strict CSP (`default-src 'none'; style-src 'sha256-...'; base-uri 'none'; form-action 'none';`) using SHA-256 hashes for inline styles. Any future modifications to inline CSS or additions of scripts/assets will require updating these CSP tags and recalculating hashes.

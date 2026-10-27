## 2026-10-27 - [Add strict Content Security Policy to static site]
**Vulnerability:** Missing security headers (CSP) allowing potential cross-site scripting (XSS), unwanted external resource loading, and unauthorized form submissions.
**Learning:** Even purely static HTML sites without external assets or build systems are susceptible to XSS if a browser plugin or network attack injects malicious scripts. Adding a strict `<meta>` CSP provides defense-in-depth where HTTP headers cannot easily be set.
**Prevention:** Always include a strict Content Security Policy, using `<meta>` tags when HTTP headers aren't available, locking down `default-src`, `script-src`, `base-uri`, and `form-action` for purely static informational sites.

## 2023-10-28 - Missing Content Security Policy on Static Site
**Vulnerability:** The static HTML site lacked a Content Security Policy (CSP), which provides defense-in-depth against XSS and other injection attacks, even though there's no dynamic content.
**Learning:** Even purely static sites should implement a strict CSP (e.g., `default-src 'none'; style-src 'unsafe-inline'`) to prevent external scripts, frames, or other unwanted resources from executing if the HTML is ever modified or served unexpectedly.
**Prevention:** Always add a basic, restrictive `<meta http-equiv="Content-Security-Policy">` tag to static HTML files.

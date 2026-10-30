## 2024-05-15 - Missing Content Security Policy (CSP)
**Vulnerability:** Purely static HTML site lacking a Content Security Policy (CSP), theoretically allowing for Cross-Site Scripting (XSS) if future changes introduce dynamic elements or user input handling.
**Learning:** Even entirely static sites with inline CSS should employ a restrictive CSP (like `default-src 'none'; style-src 'unsafe-inline'; base-uri 'none'; form-action 'none';`) to establish a defense-in-depth posture against future changes.
**Prevention:** Implement strict CSPs by default on all projects, loosening restrictions only when specifically required by new features (e.g., adding a script tag).

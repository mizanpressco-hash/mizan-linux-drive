## 2026-10-29 - [Security Enhancement] Add Content Security Policy
**Vulnerability:** Missing Content Security Policy (CSP).
**Learning:** This is a static HTML repository, so adding a restrictive CSP prevents the loading of external resources, protecting against XSS or unwanted resource injections if the HTML ever contains dynamic content or user-supplied data in the future.
**Prevention:** Always add a strict CSP to HTML pages, even static ones, for defense in depth.

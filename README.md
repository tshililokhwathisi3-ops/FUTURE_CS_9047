# Vulnerability Assessment Report — testphp.vulnweb.com

**Future Interns — Cyber Security Task 1 (2026)**
**Author:** Maxwel

## Website Tested
`http://testphp.vulnweb.com` — a public demo site intentionally provided by Acunetix for security learners to practice on.

## Scope
- Read-only, passive analysis only
- Public-facing pages only
- No login bypass, exploitation, brute-forcing, or denial-of-service activity was performed

## Tools Used
- [SecurityHeaders.com](https://securityheaders.com) — automated HTTP security header scan
- [SSL Labs (Qualys)](https://www.ssllabs.com/ssltest/) — TLS/HTTPS configuration check
- Browser DevTools — manual inspection of response headers, cookies, and page source

## Summary of Findings

| ID | Finding | Risk |
|----|---------|------|
| F-01 | Site served without encryption (no HTTPS) | High |
| F-02 | Login form reachable over plain HTTP | High |
| F-03 | Missing recommended security headers (CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy) | Medium |
| F-04 | Missing HTTP Strict Transport Security (HSTS) | Medium |
| F-05 | Indications of an outdated backend technology stack | Medium |
| F-06 | Server software version disclosed in responses | Low |
| F-07 | Cookies missing Secure / HttpOnly attributes | Medium |

Full details, business-friendly explanations, and remediation steps for each finding are in the report PDF.

## Repository Contents
```
/report
  Vulnerability_Assessment_Report.pdf   — full report
/evidence
  securityheaders-scan.png              — SecurityHeaders.com result
  ssllabs-scan.png                      — SSL Labs scan result
  devtools-headers.png                  — DevTools response headers
  devtools-cookies.png                  — DevTools cookie inspection
README.md
```

## Disclaimer
This assessment is a training exercise performed against a publicly designated test target under a strict read-only, passive scope. No real client or production system was tested.

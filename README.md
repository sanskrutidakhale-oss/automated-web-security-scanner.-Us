# Automated Web Security Header Scanner

**IBM SkillsBuild Cyber Security 2026 — BharatCares project**

**Student:** Sanskruti Dakhale  
**Institution:** Sandip University  
**Year:** Second Year  
**Submission date:** 23 October 2026

## Overview
A beginner-friendly Python tool that requests one web page and reviews six common browser security headers, basic HTTPS use, response status, and the observed CORS response header. It prints a readable report.

## Features
- Checks Content-Security-Policy (CSP)
- Checks Strict-Transport-Security (HSTS)
- Checks X-Content-Type-Options
- Checks X-Frame-Options
- Checks Referrer-Policy
- Checks Permissions-Policy
- Reports HTTP status, final URL, HTTPS use, and a basic CORS observation
- Uses a timeout and makes a single GET request; it does not exploit vulnerabilities

## Requirements
- Python 3.9 or newer
- Internet access
- `requests` library

## Setup
```bash
python -m venv .venv
```
Activate the environment:
- Windows: `.venv\\Scripts\\activate`
- macOS/Linux: `source .venv/bin/activate`

Install dependencies:
```bash
pip install -r requirements.txt
```

## Run
```bash
python web_security_scanner.py
```
Enter a URL only if you own the website or have explicit permission to assess it. Example: `https://example.com`.

## Run in Jupyter Notebook
Open `SanskrutiDakhale_AutomatedWebScanner.ipynb` in Jupyter Notebook or Google Colab and run the cells in order. Change the target URL only to an authorized test site.

## Understanding results
A missing header is a prompt for review, not automatic proof of a vulnerability. Security requirements depend on the website's architecture and intended behavior. A wildcard CORS header is not automatically unsafe; assess the endpoint and credential behavior in context. The scanner does not test authentication, TLS configuration in depth, server-side logic, or exploitability.

## Dataset / source
This project does not require a dataset. It inspects live HTTP response headers from the authorized URL supplied by the user. Reference documentation:
- MDN HTTP headers: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
- OWASP Secure Headers Project: https://owasp.org/www-project-secure-headers/
- Requests documentation: https://requests.readthedocs.io/

## Limitations
- One GET request per scan; results can vary by route, redirects, user agent, and server configuration.
- Does not crawl a site or perform penetration testing.
- Does not send exploit payloads.
- Some security controls may be enforced elsewhere (for example, at a CDN or reverse proxy).

## Ethical use
Use only on systems you own or have written permission to test. Respect rate limits, terms of service, privacy, and applicable laws. This project is for educational use and is not a substitute for a professional security assessment.

## Files
- `web_security_scanner.py` — runnable command-line scanner
- `SanskrutiDakhale_AutomatedWebScanner.ipynb` — notebook version
- `requirements.txt` — Python dependency list
- `SanskrutiDakhale_ProjectReport.docx` — project report

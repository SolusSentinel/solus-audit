# solus-audit
# WordPress Security Assessment — WPScan (Homelab)

**Author:** Danny — Solus Sentinel  
**Date completed:** 2025-09-23

---

## Overview
This is a sanitized, public record of a controlled WordPress security assessment performed in my homelab. The goal was to enumerate users/plugins/themes and validate credential strength using WPScan and Hydra. All testing was conducted on systems I own and control.

## Environment
- Kali Linux (homelab VM)
- Target: Local WordPress instance (internal IP; omitted for public repo)
- Tools: WPScan, Hydra, Nmap, GTMetrix, SSL Labs

---

## Objectives
1. Enumerate WordPress users, plugins, and themes.  
2. Check for known vulnerable plugins.  
3. Perform a controlled brute-force test against test accounts.  
4. Produce remediation recommendations.

---
## High-level Process
1. Verified the target is a homelab instance and snapshotted the VM.  
2. Ran WPScan for enumeration and vulnerability checks:
3. Reviewed WPScan output and flagged plugin versions for review.  
4. Performed a controlled Hydra test against a test account with a small wordlist and low concurrency.  
5. Captured screenshots and compiled remediation guidance.

> Note: Commands above are examples. Exact outputs and sensitive logs are intentionally omitted from this public repo.

---

## Key Findings (sanitized)
- Enumerated test users (test accounts only).  
- Flagged one out-of-date plugin in the homelab instance (non-production).  
- Controlled brute-force tests validated that weak passwords on test accounts succeeded.

---

## Recommendations
- Enforce strong passwords and enable account lockout after repeated failures.  
- Implement Two-Factor Authentication (2FA) for admin/editor accounts.  
- Keep plugins and themes updated; remove unmaintained plugins.  
- Implement rate-limiting/WAF and monitor logs for repeated failed logins.

---

## Screenshots (public-safe)
- `screenshots/wpscan-summary.png` — WPScan summary (redacted).  
- `screenshots/gtmetrix-summary.png` — performance snapshot.

---

## Artifacts & Redaction
- Full raw logs (Hydra, WPScan output with tokens/passwords) are stored privately and are not included here.  
- Do not use this repo to run scans against third-party systems. Always obtain written authorization.

---

## Next steps
- Convert remediation checklist into a client PDF.  
- Post a short case-study excerpt on LinkedIn/IG and link this repo as proof of work.

---

If you want a PDF or one-page summary version of this for clients, I can generate the text now for you to export.
1. Verified the target is a homelab instance and snapshotted the VM.  
2. Ran WPScan for enumeration and vulnerability checks:  

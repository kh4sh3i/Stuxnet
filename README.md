# 🐍 Stuxnet — Overview

Stuxnet is a highly sophisticated piece of malware discovered in 2010 that targeted Siemens Step7/WinCC industrial control systems. It used multiple zero‑day vulnerabilities and stolen digital certificates to spread and to subvert specific PLCs. This repo is meant for historical study, detection, and defensive readiness only.

## 🧰 Technical snapshot (non-actionable)

Below are public CVE identifiers commonly associated with Stuxnet analyses. These are provided for attribution and defensive tracking (patching / detection) — not to instruct exploitation.

* **CVE-2010-2568** — Windows Shell shortcut (.LNK/.PIF) remote code execution vulnerability (used to auto‑execute code when an icon was displayed).
* **CVE-2010-2729** — Windows Print Spooler remote code execution / impersonation vulnerability (printer‑sharing related).
* **CVE-2010-2743** — Win32k keyboard‑layout handler privilege escalation (kernel‑mode elevation of privilege used in some Stuxnet variants).
* **CVE-2010-2772** — Siemens SIMATIC WinCC / Step7 authentication/hard‑coded credential weakness used by Stuxnet to target SCADA components.

## 🛡️ Defensive recommendations (high level)

* Ensure all systems (Windows and ICS engineering stations) are patched and not running unnecessary services (e.g., printer sharing).
* Harden removable‑media policies and monitor USB activity.
* Monitor for known IOCs and suspicious Step7/WinCC changes; implement file integrity monitoring for engineering workstations.

## 📚 References (examples of sources to read)

* Vendor advisories (Symantec / Microsoft / CERT / ICS‑CERT) and reputable writeups (Kaspersky, Wired, academic papers). See `REFERENCES.md` for curated links.



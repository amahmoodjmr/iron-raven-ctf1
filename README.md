# CIP-A105 — Offensive Security Operations II — CTF 1: Operation Iron Raven

**Student:** Abubakar Mahmood Muhammad (Sadeeq)
**Registration Number:** C11/26/EHIT/17332
**Target:** OPFOR-01 (raven.local / 192.168.72.130)
**Assessment Window:** 06 Sep 2026 00:00 WAT – 13 Sep 2026 23:59 WAT
**Submission Date:** 15/09/2026
**Classification:** TRAINING USE ONLY — DO NOT REDISTRIBUTE

## Contents

```
/report
  Iron_Raven_Report_Draft.docx   — Full assessment report (executive summary,
                                    methodology, findings IR-001–IR-004,
                                    risk register, remediation roadmap,
                                    lessons learned, appendices)

/evidence/screenshots
  01–60  — Chronologically numbered screenshots covering reconnaissance,
           attack-surface enumeration, vulnerability analysis, and
           controlled authentication testing, matching the Operator
           Activity Log in the report (Appendix A)

/evidence/logs
  file_hashes.txt — SHA256 hash of the recovered mission artifact (flag3.png)
```

## Summary of Outcome

- Reconnaissance and full attack-surface enumeration completed (nmap, gobuster,
  whatweb, nikto).
- One confirmed vulnerability (Apache directory listing on
  `/wp-content/uploads/`) led to recovery of mission artifact **flag3**.
- WordPress core (4.8.7) and Akismet (3.3.2) versions were researched against
  NVD and the WPScan Vulnerability Database; the specific CVEs reviewed were
  determined not to apply, as each had already been patched prior to the
  installed version. This elimination process, including the reasoning for
  each ruled-out candidate, is documented in Finding IR-002.
- A controlled, rate-limited, individually-logged authentication test was
  conducted against the WordPress XML-RPC interface and SSH service using a
  small set of documented candidate passwords. No valid credentials were
  identified within the assessment window (Findings IR-003, IR-004).
- flag1 and flag2 were not recovered within the assessment window.

Full reasoning, evidence, and remediation guidance are documented in the
report under `/report`.

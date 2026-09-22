# CIP-A105 CTF 2 — Operation Black Forge

**Offensive Security Operations II — Summative Competency Exam**

Target: OPFOR-02 (Healthcare OVA) — 192.168.56.109
Classification: TRAINING USE ONLY

---

## Package Contents

| Folder | Contents |
|--------|----------|
| `report/` | Professional PDF report (Executive + Technical + Risk Register + Lessons Learned) |
| `Evidence/` | Numbered evidence E-01 through E-29 |
| `Annexes/` | Operator Activity Log (Annex B) |
| `README.txt` | Submission manifest and integrity verification |

---

## Mission Summary

| Item | Value |
|------|-------|
| Initial Access | OpenEMR 4.1.0 SQL injection → admin credential recovery |
| Foothold | File upload RCE via Patient Documents (apache uid 479) |
| Privilege Escalation | PATH hijack on SUID `/usr/bin/healthcheck` |
| User Flag | `d41d8cd98f00b204e9800998ecf8427e` |
| Root Flag | `eaff25eaa9ffc8b62e3dfebf70e83a7b` |

---

## Rules of Engagement Compliance

- Only the Academy-issued OPFOR-02 target was tested.
- No external or production systems were accessed.
- Target restored to CIP-A105-CTF2-CLEAN-BASELINE after evidence collection.
- No learner artifacts remain on the target.

---

## Report Sections

1. Executive Summary
2. Scope and Rules of Engagement
3. Laboratory Architecture and Methodology
4. Attack-Surface Summary
5. Confirmed Findings and Risk Ratings
6. Initial-Access Narrative
7. Post-Exploitation and Privilege-Escalation Narrative
8. Mission Objectives and Proof of Completion
9. Attack-Path Diagram
10. Remediation Roadmap
11. Conclusion and Lessons Learned
12. Appendices

---

*Prepared by: Loveth Adebayo*

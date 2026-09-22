============================================================
OPERATION BLACK FORGE — SUBMISSION PACKAGE
CIP-A105 CAPTURE-THE-FLAG 2 — SUMMATIVE COMPETENCY EXAM
============================================================

Student Name:       Loveth Adebayo
Registration No:    C11/26/EHIT/17323
Submission Date:    22 September 2026
Classification:     TRAINING USE ONLY — DO NOT REDISTRIBUTE

------------------------------------------------------------
PACKAGE CONTENTS
------------------------------------------------------------

01_Report/
    CIP-A105_CTF2_Black-Forge_Report.pdf
        Main professional report containing:
        - Cover page
        - Executive summary
        - Scope and Rules of Engagement
        - Laboratory architecture and methodology
        - Attack-surface summary
        - Confirmed findings and risk ratings
        - Initial-access narrative
        - Post-exploitation and privilege-escalation narrative
        - Mission objectives and proof of completion
        - Attack-path diagram
        - Remediation roadmap
        - Conclusion and lessons learned
        - Appendices (evidence index, risk register)

02_Evidence/
    Evidence E-01 through E-29
        Raw screenshots, terminal outputs, and text logs
        referenced throughout the report. File names match
        the evidence references in the report.

    evidence_register.csv
        Tabular index of all evidence files with timestamps,
        sources, and purposes.

03_Annexes/
    ANNEX_B_Operator_Activity_Log.txt
        Complete chronological activity log recording every
        command, tool, observation, and evidence reference,
        including failed hypotheses and abandoned paths.

------------------------------------------------------------
MISSION SUMMARY
------------------------------------------------------------

Target:             OPFOR-02 (Healthcare OVA)
Target IP:          192.168.56.109
Attacker:           Kali Linux (192.168.56.105)
Network:            Isolated Host-Only (vboxnet0, 192.168.56.0/24)

Attack Chain:
    1. Reconnaissance     nmap, netdiscover
    2. Web Enumeration    gobuster -> /openemr/ discovered
    3. SQL Injection      validateUser.php -> sqlmap
    4. Credential Dump    openemr.users table
    5. Password Crack     admin:ackbar recovered
    6. Initial Access     OpenEMR admin dashboard
    7. RCE                Patient document upload (cmd.php)
    8. Foothold           apache user (uid 479)
    9. Post-Exploitation  SUID /usr/bin/healthcheck identified
   10. Privilege Escalation  PATH hijack -> SUID /tmp/rootbash
   11. Root Access       euid=0(root)

Mission Proofs:
    User Flag:          d41d8cd98f00b204e9800998ecf8427e
    Root Flag:          eaff25eaa9ffc8b62e3dfebf70e83a7b

------------------------------------------------------------
RULES OF ENGAGEMENT COMPLIANCE
------------------------------------------------------------

- All activity was performed only against the Academy-issued
  OPFOR-02 target.
- No external or production systems were accessed.
- Bridged networking and public internet exposure were
  disabled throughout the engagement.
- No denial-of-service, destructive actions, or privilege
  escalation beyond the defined objective were performed.
- Persistence was not maintained; all artifacts were
  removed after evidence collection.
- The target was restored to the CIP-A105-CTF2-CLEAN-BASELINE
  snapshot after the operation.
- No personal, Academy production, or third-party
  confidential data was introduced into the lab.
- No target-specific walkthroughs, solution videos, or
  answer-sharing materials were used.

------------------------------------------------------------
INTEGRITY VERIFICATION
------------------------------------------------------------

Target OVA integrity was verified before import:

    MD5:    3D64CFFCDAADBF683ACDB0E4BF8FBC47     (match)
    SHA1:   7E65804C291C3453F75D83F6A280A4440ADFE104  (match)

------------------------------------------------------------
SUBMISSION NOTES
------------------------------------------------------------

- The report is a single professional PDF as required by
  the Operations Brief (Section 12).
- All evidence is numbered and cross-referenced with the
  report.
- The operator activity log is provided as a standalone
  Annex B file for convenience.
- No original VM image is included in this package.

------------------------------------------------------------
END OF README
============================================================

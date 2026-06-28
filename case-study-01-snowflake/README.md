# MITRE ATT&CK Case Studies

This repository contains my analysis of real-world cybersecurity incidents using the MITRE ATT&CK framework. Each case study follows the attacker lifecycle from initial access to post-incident response, mapping observed attacker behavior to MITRE ATT&CK while identifying practical detection opportunities and defensive mitigations.

My objective is not simply to assign ATT&CK techniques, but to understand **why** attackers performed specific actions, **how** those actions align with ATT&CK, and **what defenders could have done** to detect or disrupt the attack.

All mappings are based on publicly available incident reports and security research. Where public evidence does not support mapping to a specific ATT&CK sub-technique, the analysis intentionally remains at the technique level.

---

# Repository Structure

Each case study follows the same structure:

```text
01-incident-summary.md     → Overview of the incident and key lessons
02-attack-timeline.md      → Chronological reconstruction of attacker activity
03-mitre-mapping.md        → MITRE ATT&CK tactics, techniques and supporting evidence
04-detections.md           → Detection opportunities and potential indicators
05-mitigations.md          → Security recommendations and defensive controls
references.md              → Public sources and threat intelligence references
```

---

# Current Case Studies

## Case Study 01 – Snowflake Customer Data Breaches (2024)

This case study examines the 2024 Snowflake customer data breaches, where attackers used compromised legitimate credentials to access customer environments and steal sensitive data.

The analysis includes:

* Identity-based initial access using valid cloud accounts
* Environment discovery and reconnaissance
* Data collection and staging
* Data exfiltration
* MITRE ATT&CK mapping with supporting evidence
* Detection opportunities for defenders
* Security mitigations and lessons learned

---

# Planned Case Studies

The repository will continue to grow with additional analyses of real-world incidents, including:

* Marks & Spencer Cyberattack
* Coinbase Data Breach
* Additional cloud and enterprise security incidents

---

# Skills Demonstrated

Through these case studies, I practice and demonstrate:

* MITRE ATT&CK Mapping
* Incident Analysis
* Threat Analysis
* Detection Engineering Concepts
* Identity Security
* Cloud Security
* Security Monitoring
* Security Controls and Mitigations
* Technical Documentation

---

# Disclaimer

This repository is intended for educational purposes. The analysis is based on publicly available reporting from incident responders, security vendors, and official disclosures. ATT&CK mappings represent my evidence-based interpretation of documented attacker behavior and are intended to support learning and discussion rather than serve as an authoritative incident report.

# MITRE ATT&CK Case Studies

This repository contains a collection of real-world cybersecurity incident analyses using the MITRE ATT&CK framework.
Each case study reconstructs the attacker lifecycle from publicly available reporting and maps observed attacker behavior 
to MITRE ATT&CK tactics and techniques.

The objective of this repository is to strengthen my understanding of attacker tradecraft while developing practical skills 
in incident analysis, threat detection, cloud security, and defensive security engineering.

Rather than simply assigning ATT&CK techniques, each case study focuses on answering five questions:

1. **What happened?**
2. **How did the attacker progress through the environment?**
3. **How does the activity map to MITRE ATT&CK?**
4. **How could defenders detect the attack?**
5. **What security controls could have prevented or limited the impact?**

---

# Repository Structure

Each case study follows the same structure:

```text
case-study-xx/

├── 01-incident-summary.md
├── 02-attack-timeline.md
├── 03-mitre-mapping.md
├── 04-detections.md
├── 05-mitigations.md
└── references.md
```

---

# Case Studies

| Case Study                              | Status         |
| --------------------------------------- | -------------- |
| Snowflake Customer Data Breaches (2024) | ✅ Complete     |
| Marks & Spencer Cyberattack             | 🚧 In Progress |
| Coinbase Data Breach                    | 📅 Planned     |

Additional real-world case studies will be added over time.

---

# Skills Demonstrated

This repository demonstrates practical experience in:

* MITRE ATT&CK Mapping
* Incident Analysis
* Threat Intelligence
* Detection Engineering
* Threat Hunting Concepts
* Identity Security
* Cloud Security
* Security Monitoring
* Security Controls and Mitigations
* Technical Documentation

---

# Methodology

Each analysis is based on publicly available incident reports, threat intelligence research, and the MITRE ATT&CK framework.

Where public evidence does not support mapping to a specific ATT&CK sub-technique, the analysis intentionally remains at the
technique level. All ATT&CK mappings are evidence-based and supported by documented attacker behavior rather than assumptions.

---

# Purpose

This repository is part of my cloud security and cybersecurity learning journey. My goal is to improve my ability to analyze 
real-world incidents, understand attacker behavior, and think from both an offensive and defensive security perspective.

---

# Disclaimer

This repository is intended for educational purposes only. The analyses are based on publicly available information and
represent my interpretation of documented attacker activity. They are not official incident reports.

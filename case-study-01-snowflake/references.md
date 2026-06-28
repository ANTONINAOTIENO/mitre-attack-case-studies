# References

The analysis in this case study is based on publicly available incident reporting, threat intelligence, and the MITRE ATT&CK framework.

## Primary Incident Sources

1. Mandiant. **UNC5537 Targets Snowflake Customer Instances for Data Theft and Extortion.** Google Cloud Threat Intelligence Blog (June 2024).
   https://cloud.google.com/blog/topics/threat-intelligence/unc5537-snowflake-data-theft-extortion

   *Primary source describing the UNC5537 campaign, attack timeline, observed SQL commands, attacker behavior, and security recommendations.*

---

## Detection & Threat Hunting

2. Datadog Security Labs. **A Guide to Threat Hunting and Monitoring in Snowflake.**
   https://securitylabs.datadoghq.com/articles/a-guide-to-threat-hunting-and-monitoring-in-snowflake/

   *Referenced for detection opportunities, monitoring strategies, and examples of suspicious activity within Snowflake environments.*

---

## Framework References

3. MITRE ATT&CK®. **MITRE ATT&CK Enterprise Matrix.**
   https://attack.mitre.org/tactics/enterprise/

   *Referenced to map observed attacker behavior to ATT&CK tactics, techniques, and sub-techniques.*

---

## Analyst Notes

* ATT&CK mappings represent my interpretation of publicly documented attacker behavior.
* Where public evidence did not support mapping to a specific sub-technique, the analysis intentionally remained at the technique level.
* Detection opportunities and mitigations were developed using information from the referenced incident reports together with MITRE ATT&CK guidance.

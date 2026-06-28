# MITRE ATT&CK Mapping

## Precondition

## MITRE Mapping: None

### Reason: Outside the scope of this incident analysis.

*Note that the credential compromise that enabled this campaign is acknowledged as a precondition but is not mapped in this report because it occurred prior to the documented intrusion into Snowflake customer environments.

*Analyst Note: ATT&CK mappings are based on publicly documented attacker behavior from incident reporting by Mandiant and other public sources. Where public evidence does not support mapping to a specific sub-technique, the mapping is intentionally limited to the technique level.


| Timeline Step          | ATT&CK Tactic  | Technique                      | Technique ID | Sub-technique              | Justification                                                                                                                                                                                                                                                                                            |
| ---------------------- | -------------- | ------------------------------ | ------------ | -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Initial Authentication | Initial Access | Valid Accounts                 | T1078        | T1078.004 – Cloud Accounts | The attackers successfully authenticated to targeted Snowflake customer environments using compromised legitimate cloud account credentials, establishing an initial foothold without exploiting a software vulnerability.                                                                               |
| Environment Discovery  | Discovery      | Cloud Storage Object Discovery | T1619        | N/A                        | After gaining access, the attackers enumerated accessible cloud-hosted datasets and storage objects to identify valuable information for theft. Public reporting showed the use of reconnaissance commands such as `SHOW TABLES` to discover available databases and tables before collecting data.      |
| Data Collection        | Collection     | Data from Cloud Storage        | T1530        | N/A                        | Once valuable datasets had been identified, the attackers retrieved the targeted information from the compromised Snowflake environment using SQL queries such as `SELECT * FROM`. They then staged the data using temporary Snowflake stages (`CREATE TEMP STAGE`) and `COPY INTO` before exfiltration. |
| Data Exfiltration      | Exfiltration   | Exfiltration Over Web Service  | T1567        | N/A                        | After staging the collected data, the attackers transferred it outside the victim environment. Public reporting showed the use of the `GET` command to retrieve staged data from Snowflake, completing the exfiltration phase of the attack.    


Although the attackers used Snowflake stages during the operation, public reporting specifically documented the use of the GET command to retrieve data to attacker-controlled local systems. Therefore, the exfiltration is mapped to T1567 rather than the more specific T1567.002 (Exfiltration to Cloud Storage).



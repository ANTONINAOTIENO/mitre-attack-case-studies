# Snowflake Customer Data Breaches (2024)

**Industry:** Cloud Computing / Data Platform

**Attack Type:** Credential-based Data Breach

**Primary ATT&CK Tactic:** Initial Access

**Affected Organizations:** AT&T, Ticketmaster, Santander, Advance Auto Parts, others

**Primary Security Domain:** Identity Security

## Objectives

This case study analyses the 2024 Snowflake customer data breaches using the MITRE ATT&CK framework to understand how the attackers gained access, navigated customer environments, collected sensitive information, and exfiltrated data. The objective is to identify attacker behavior, map it to ATT&CK tactics and techniques, and highlight practical detection and mitigation opportunities for cloud security teams.
This analysis is intended as both a learning exercise in applying the MITRE ATT&CK framework and a practical incident review for improving cloud security and identity protection practices.


## Executive Summary

In 2024, a series of high-profile data breaches affected multiple Snowflake customers after attackers gained unauthorized access to customer environments using valid credentials. Once authenticated, the attackers searched for valuable datasets, collected sensitive customer information, and exfiltrated the data, resulting in significant financial losses, reputational damage, and the exposure of customer information.

Public investigations indicated that many of the affected accounts did not have multi-factor authentication (MFA) enabled. While the attackers authenticated using legitimate credentials, the absence of MFA reduced an important layer of defense and contributed to the success of the compromise. The incident demonstrates how identity-based attacks can bypass traditional security controls when valid accounts are abused.

This case highlights several important lessons for security professionals. Strong identity security, including enforcing MFA, promoting good password hygiene, and responding quickly to known credential exposures, remains essential for protecting cloud environments. Equally important is continuous monitoring of authentication events, account activity, and data access patterns to detect suspicious behavior early and reduce the impact of a compromise. Ultimately, the Snowflake incident reinforces that cloud security is fundamentally dependent on protecting identities as much as protecting infrastructure.


## Incident background

Snowflake is a cloud-based data platform that enables organizations to securely store, manage, and analyze large volumes of data. Rather than the platform itself being broadly compromised, the 2024 incident primarily affected a number of Snowflake customers whose environments were accessed through compromised legitimate credentials.

Several well-known organizations, including AT&T, Ticketmaster, and Santander, publicly disclosed that they had been affected by the campaign. Public reporting indicated that many of the credentials used by the attackers had previously been exposed through infostealer malware, and many of the affected customer accounts did not have multi-factor authentication (MFA) enabled. These conditions allowed attackers to successfully authenticate and access customer environments.

The incident attracted significant attention because it affected multiple high-profile organizations and resulted in the unauthorized access and exfiltration of sensitive customer data. Beyond the immediate financial and reputational impact on the affected organizations, the incident highlighted the growing importance of identity security within cloud environments. It demonstrated that cloud platforms can remain secure while customer environments are still compromised through the misuse of valid credentials, reinforcing the need for strong authentication controls and continuous monitoring.


## Scope of Analysis
This report focuses on the publicly documented attack lifecycle against affected Snowflake customer environments. It does not analyse the internal Snowflake platform or speculate on undocumented attacker activity. All ATT&CK mappings are based on publicly available reporting and observed attacker behaviour.

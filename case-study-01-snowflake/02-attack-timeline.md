# Attack Timeline

# Overview

This timeline reconstructs the sequence of attacker activities based on publicly documented reporting of the 2024 Snowflake
customer data breaches. The objective is to describe the attack chronologically before mapping each activity to the MITRE ATT&CK 
framework in the following section.

## Preconditions

Public reporting indicated that the attackers possessed previously compromised customer credentials, many of which had been harvested
through infostealer malware before the campaign against Snowflake customers began. These credentials enabled the attackers to authenticate
successfully to targeted customer accounts.


| Step         | Activity                              | Outcome                    |
| ------------ | ------------------------------------- | -------------------------- |
| Precondition | Possession of compromised credentials | Enabled authentication     |
| 1            | Authentication                        | Access established         |
| 2            | Discovery                             | Valuable assets identified |
| 3            | Collection                            | Data prepared for theft    |
| 4            | Exfiltration                          | Data stolen                |
| Response     | Incident response                     | Containment and recovery   |


# Timeline Step 1 – Initial Authentication

## Attacker Action

After obtaining previously compromised credentials, the attackers attempted to authenticate to targeted Snowflake customer
accounts. The authentication was successful because the credentials were valid, allowing the attackers to establish access 
to the affected customer environments.

### Why this step matters

Successful authentication established the attacker's foothold within the customer environment and enabled all subsequent stages 
of the intrusion.


# Timeline Step 2 – Environment Discovery

## Attacker Action

After successfully authenticating, the attackers explored the customer environment to understand what resources were accessible 
using the compromised account. They identified databases, datasets, and other accessible information to determine which assets 
were most valuable and worth targeting. This reconnaissance allowed them to plan the next stage of the attack before collecting
any data.

### Why this step matters

Reconnaissance allowed the attackers to understand the environment and prioritize high-value datasets before attempting to steal them.


# Timeline Step 3 – Data Collection

## Attacker Action

After identifying valuable datasets during their reconnaissance, the attackers gathered the targeted information in preparation for 
exfiltration. They organized the data they intended to steal, ensuring that the selected datasets could be transferred to attacker-controlled
infrastructure during the next stage of the attack.

### Why this step matters

Collecting the identified datasets ensured the attackers had assembled the information required to accomplish their objective before transferring
it outside the environment. 


# Timeline Step 4 – Data Exfiltration

## Attacker Action

After gathering the targeted datasets, the attackers transferred the stolen information from the affected Snowflake customer environments to attacker-controlled
infrastructure. At this stage, sensitive customer data left the victim's environment, allowing the attackers to achieve their primary objective of data theft.

### Why this step matters

Once data left the customer environment, the organization's confidentiality was compromised and the attackers had successfully achieved their primary objective.


# Post-Incident Response

Following the discovery of the breaches, the affected organizations initiated incident response procedures to investigate the scope of the compromise and determine
which customer data had been accessed. Containment measures included resetting compromised credentials, strengthening authentication controls, increasing monitoring 
of account activity, and notifying affected customers and regulatory authorities where required. The incident also prompted stronger recommendations and, in many cases,
requirements for customers to enable multi-factor authentication (MFA) and adopt improved identity security practices to reduce the risk of similar attacks in the future.



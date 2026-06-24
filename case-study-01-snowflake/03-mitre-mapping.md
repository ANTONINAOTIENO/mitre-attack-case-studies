# MITRE ATT&CK Mapping

## Step 1: Access Using Legitimate Credentials

### ATT&CK Tactic

Initial Access

### ATT&CK Technique

Valid Accounts

### Justification

The attackers successfully authenticated using legitimate credentials associated with Snowflake customer accounts. Because the attackers used real accounts rather than exploiting a software vulnerability, the activity aligns with the ATT&CK technique "Valid Accounts."



## Step 2: Identifying Valuable Data

### ATT&CK Tactic

Discovery

### ATT&CK Technique

Cloud Service Discovery

### Justification

After gaining access, the attackers needed to understand the environment and identify valuable datasets. This activity aligns with Discovery because the attackers were gathering information about available resources before selecting data for theft.



## Step 3: Collecting data

### ATT&CK Tactic
Collection


### Justification
After identifying valuable datasets, the attackers gathered and prepared the information they intended to steal. This activity aligns with Collection because the attackers were actively obtaining the target data before transferring it outside the environment.



## Step 4: Exporting Data

### ATT&CK Tactic
Exfiltration

### Justification
The attacker has collected the valuable data and has staged it for exfiltration/exportation. At this poing there may be large downloads of the valuable data identified from the accounts into their server. This activity aligns with Exfiltration because the data is exiting the account premises.
...

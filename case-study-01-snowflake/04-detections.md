# Detection Opportunities

## Suspicious Login Activity

Potential indicators:

- Multiple failed login attempts
- Login from unusual geographic locations
- Impossible travel events
- Login outside normal working hours
- Login from previously unseen devices

  
| Attack Stage           | Detection Opportunity                                 | Why it Matters                                                                                       |
| ---------------------- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Initial Authentication | Impossible travel detection                           | May indicate valid credentials are being used from geographically impossible locations.              |
| Initial Authentication | Authentication outside normal user activity           | Helps identify compromised accounts being accessed at unusual times.                                 |
| Initial Authentication | Login from a new device or browser                    | May indicate a legitimate account is being accessed from an unfamiliar endpoint.                     |
| Initial Authentication | Authentication without MFA                            | High-risk logins without MFA significantly increase the likelihood of successful account compromise. |
| Initial Authentication | Multiple failed logins followed by a successful login | May indicate password spraying or credential guessing preceding a successful compromise.             |


  
## Suspicious Discovery Activity

During the discovery phase, defenders should monitor for behavior that indicates an attacker is exploring the environment to identify valuable assets before data theft.

**Potential indicators:**

* Enumeration of databases, schemas, tables, or storage objects (for example, repeated `SHOW TABLES` commands)
* Repeated queries to identify accessible datasets and resources
* Access to databases or datasets outside the user's normal business function
* Enumeration of cloud storage objects or repositories that the user does not typically access
* Unusual spikes in metadata queries or reconnaissance activity within the environment

---

## Suspicious Data Collection Activity

Once valuable information has been identified, attackers typically begin gathering the data before transferring it outside the environment.

**Potential indicators:**

* Large-volume SQL queries against sensitive databases
* Repeated `SELECT` queries targeting customer or personally identifiable information (PII)
* Creation of temporary stages or staging locations that are not part of normal business operations
* Large datasets being copied into temporary storage (`COPY INTO`) for later export
* Data access volumes significantly exceeding the user's normal activity baseline

---

## Suspicious Data Exfiltration Activity

After staging the data, defenders should monitor for activity consistent with unauthorized data export.

**Potential indicators:**

* Large or unexpected data downloads from Snowflake environments
* Execution of data export commands such as `GET`
* Sudden increases in outbound data transfer volume
* Data exports occurring outside normal business hours
* Data transfers performed by accounts that do not normally export large datasets
* Multiple export operations occurring within a short period of time

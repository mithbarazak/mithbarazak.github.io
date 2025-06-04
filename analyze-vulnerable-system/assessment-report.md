# **Vulnerability Assessment Report**

## **1st January 20XX**

## ---

# **System Description**

The server hardware consists of a powerful CPU processor and 128GB of memory. It runs on the latest version of Linux operating system and hosts a MySQL database management system. It is configured with a stable network connection using IPv4 addresses and interacts with other servers on the network. Security measures include SSL/TLS encrypted connections.

# **Scope**

The scope of this vulnerability assessment relates to the current access controls of the system. The assessment will cover a period of three months, from June 20XX to August 20XX. **NIST SP 800-30 Rev. 1** is used to guide the risk analysis of the information system.

# **Purpose**

The server in question hosts a database that is used on a daily basis by employees around the world to perform necessary business functions as well as to seek out new potential customers. Because the database is vital to daily business functions if the database is inaccessible it will disrupt the flow of business. Additionally, because both current and potential clients’ personally identifiable information (PII) is stored within the database, we have a legal and ethical obligation to keep this data secure.

# **Risk Assessment**

| Threat source | Threat event | Likelihood | Severity | Risk |
| :---- | :---- | :---- | :---- | :---- |
| *E.g. Competitor* | *Obtain sensitive information via exfiltration* | *1* | *3* | *3* |
| *Employee* | *Alter/Delete critical information (intentionally or accidentally)* | *1* | *3* | *3* |
| *Competitor* | *Conduct Denial of Service (DoS) attacks.* | *2* | *3* | *6* |
| *Hacker* | *Craft counterfeit certificates* | *2* | *3* | *6* |

# **Approach**

For this exercise I opted for a broad top-level approach, selecting a variety of threat actors and most likely threat events for each rather than focusing on the most likely events which would come from less varied sources. A more comprehensive assessment would require significantly more time and access to the current server configuration. Without the ability to access the current configuration, these seemed the most likely threats from these particular sources.

# **Remediation Strategy**

Based on the limited number of threats present in this assessment I recommend the following remediation efforts, in order of risk.

To address a hacker crafting counterfeit certificates we need to implement regular security audits of user accounts and privileges. By regularly monitoring logins through the use of SIEM tools we can recognize if any patterns of access change that might indicate an unauthorized user masquerading as an authorized user.

We also should invest in a next generation firewall (NGFW) to harden the server’s security in line with the principle of Defense In Depth. This will also help to protect against any potential DDoS attacks, as it can autonomously detect incoming packet floods and block malicious sources before server resources are overwhelmed.

To mitigate the risk of critical information getting altered or deleted, we should be conducting regular server backups, and ensuring that employees’ access privileges are limited to only what is needed for daily business tasks in line with the principle of least privilege. Regularly auditing access privileges will help to ensure that employees do not have the ability to alter critical data outside the scope of their daily duties, and regular backups ensure that if data is altered or deleted it can be restored with a minimal loss of information.

---

[Back](README.md)

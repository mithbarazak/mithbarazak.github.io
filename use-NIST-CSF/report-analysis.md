**Incident report analysis**

**Instructions**

As you continue through this course, you may use this template to record your findings after completing an activity or to take notes on what you've learned about a specific tool or concept. You can also use this chart as a way to practice applying the NIST framework to different situations you encounter.

| Summary | Recently the organization experienced an internal network outage when a malicious actor identified a vulnerability in the organization’s firewall that allowed the attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack. During the attack the organization’s network services stopped responding and normal internal network traffic was unable to access any network resources. The internal network was unavailable for two hours until the event could be fully resolved. |  |  |
| :---- | :---- | ----- | ----- |
| Identify | The incident management team audited the systems, devices, and access policies involved in the attack to identify the gaps in security. The team found that a malicious actor sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This allowed the attacker to overwhelm the company’s internal network and prevent authorized users from accessing network resources. No internal data was compromised in this attack and no employees were found to have contributed to the attack. |  |  |
| Protect | To address this incident the security team has implemented a new firewall rule to limit the rate of incoming ICMP packets, added source IP verification on the firewall to check for spoofed IP addresses on incoming ICMP packets, and added network monitoring software to detect abnormal traffic patterns. Additionally, the security team will be adding an intrusion detection/protection system (IDS/IPS). |  |  |
| Detect | Using the new intrusion protection system (IPS) and network monitoring software, the security team will be able to more quickly respond to abnormal network traffic that might signal the start of a DDoS attack. |  |  |
| Respond | To halt this attack the team blocked incoming ICMP packets and took non-critical network services offline, allowing internal network resources to recover while implementing the new firewall rules. The security team will continue to monitor network traffic to more quickly detect any future attempts to flood the network with ICMP packets. The firewall rules will continue to be maintained and updated using industry standard best practices as new vulnerabilities are found. |  |  |
| Recover | The security team restored critical network services by blocking incoming ICMP packets, stopping all non-critical network services offline, and then implementing new firewall rules. Once all network resources recovered the team was able to re-enable normal ICMP traffic using the new, more robust, firewall rules. |  |  |

---

| Reflections/Notes: |
| :---- |

---

[Back](README.md)
# dns-tunneling-detection-wireshark

#  DNS Tunneling Detection using Wireshark

This project demonstrates how to detect covert DNS tunneling activity using `Wireshark`, based on a captured PCAP file generated using the tool `dnscat2`.

---

 Objective

Analyze DNS traffic to detect data exfiltration via DNS tunneling, a method commonly used by attackers to bypass firewalls and send/receive data using the DNS protocol.

---

Tools Used

- Wireshark
- PCAP: `dnscat2_dns_tunneling_1hr.pcap` from Active Countermeasures

---

Key Indicators Found

| Indicator                        | Description |
|----------------------------------|-------------|
| Long subdomains                  | Base64-like strings indicating payloads |
| Frequent DNS queries             | Dozens of requests in short time spans |
| Same destination IP              | Constant contact with attacker's DNS server |
| UDP Stream payload               | Encoded data seen in DNS queries |

---

 Summary

- Internal IP: `10.10.2.22`
- Attacker DNS IP: `10.20.57.3`
- Technique: `dnscat2` DNS Tunneling
- Result: **Confirmed DNS-based exfiltration**

---

Learning Outcome

This project gave hands-on experience detecting real-world DNS tunneling — a key skill in blue team and SOC environments.


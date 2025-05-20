# Cybersecurity Incident Report: 

# Network Traffic Analysis

| Part 1: Provide a summary of the problem found in the DNS and ICMP  traffic log.  |  |
| :---- | ----- |
| The UDP protocol reveals that multiple DNS queries were sent from 192.51.100.15 to the DNS server at 203.0.113.2 requesting an A record for yummyrecipesforme.com. This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message: "udp port 53 unreachable." The port noted in the error message is used for DNS (Domain Name System) queries, which operate over UDP port 53\. The most likely issue is that the DNS server at 203.0.113.2 is either down, misconfigured, or blocking requests from 192.51.100.15, preventing DNS resolution for the requested domain.  |  |
|  |  |

| Part 2: Explain your analysis of the data and provide at least one cause of the incident. |
| :---- |
| Time incident occurred: 13:24:32 How the IT team became aware of the incident: Network monitoring alerts or user reports of failed DNS lookups. Actions taken to investigate: Checked connectivity between 192.51.100.15 and 203.0.113.2 3 times and received ICMP errors confirming UDP port 53 is unreachable. Key findings: DNS server (203.0.113.2) is rejecting or failing to process requests. ICMP errors confirm UDP port 53 is unreachable. Likely cause: DNS server failure due to DDoS, misconfiguration, or firewall blocking requests. Next steps: Check DNS server logs, verify firewall rules, and restart the service if needed. |


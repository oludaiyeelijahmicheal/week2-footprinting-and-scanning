# Week 2: Footprinting and Network Scanning

Penetration testing report for Week 2 of the Networkwalks Cybersecurity internship. It covers the first two phases of a pentest: reconnaissance and scanning.

## Scope and authorization
- **Target 1:** networkwalks.com (public website and DNS records), tested under the internship program's written authorization.
- **Target 2:** a local network, using host discovery only (ping scan).
- Passive and light information-gathering only. No exploitation, brute force or denial of service.

## Modules completed
| Module | Description |
|---|---|
| W2-PM1 | Footprinting with six Kali tools |
| W2-PM5 | Network scanning with Zenmap |

## Tools used
`whois` · `whatweb` · `nslookup` · `curl -I` · `wafw00f` · `dnsrecon` · Zenmap

## Key observations
| Area | Observation |
|---|---|
| Web stack | Apache, WordPress 7.1.4, WordPress Download Manager 3.3.76 |
| Hosting | Server IP 192.232.216.135, HostGator name servers, GoDaddy registrar |
| Protection | ModSecurity (SpiderLabs) WAF detected |
| DNS | Recursion enabled on name servers, DNSSEC unsigned, SPF soft fail |
| HTTP headers | REST API advertised at /wp-json/, common security headers not seen |
| Local network | 46 live hosts found with a ping scan (details withheld for privacy) |

These are observations, not confirmed vulnerabilities.

## Repository contents
- `report/`: the full report (PDF)
- `evidence/`: screenshots of each command
- `outputs/`: saved text output of each command

## Lessons learned
- Public information alone reveals a lot about a target's technology and hosting.
- Version numbers and records are leads to investigate, not proof of a vulnerability.
- Every test must stay inside an authorized scope.

## Evidence

### whois
<img width="1284" height="803" alt="whois result image" src="https://github.com/user-attachments/assets/bf80a595-2b20-4113-913f-6548c04bf65c" />

### whatweb
<img width="1281" height="802" alt="whatweb result image" src="https://github.com/user-attachments/assets/a0031f8f-5c78-4070-8290-678a721d6e00" />

### nslookup
<img width="1281" height="800" alt="nslookup result" src="https://github.com/user-attachments/assets/6f16e353-2d7f-4a21-8aa2-023e2a21352b" />

### curl -I
<img width="1278" height="801" alt="curl -I result" src="https://github.com/user-attachments/assets/a601fc8f-1350-4d03-865d-cbcc04696cda" />

### wafw00f
<img width="1280" height="800" alt="wafw00f result" src="https://github.com/user-attachments/assets/9f9426b8-0674-4f38-8150-99f94ffa07fb" />

### dnsrecon
<img width="1280" height="799" alt="dnsrecon -d result" src="https://github.com/user-attachments/assets/44a56aa1-8f25-4936-8d4c-a40f4b0ffeec" />

## Ethical use
For education only. Only test systems you own or have written permission to test.

Related: [Lab setup](https://github.com/oludaiyeelijahmicheal/cybersecurity-lab-setup) · [Wireshark SOC labs](https://github.com/oludaiyeelijahmicheal/wireshark-soc-labs)

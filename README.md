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

## Ethical use
For education only. Only test systems you own or have written permission to test.

Related: [Lab setup](https://github.com/oludaiyeelijahmicheal/cybersecurity-lab-setup) · [Wireshark SOC labs](https://github.com/oludaiyeelijahmicheal/wireshark-soc-labs)

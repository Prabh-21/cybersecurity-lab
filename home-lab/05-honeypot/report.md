# Honeypot Deployment — OpenCanary

## Tools Used
OpenCanary, Kali Linux

## What I Did
- Installed and configured OpenCanary honeypot
- Enabled fake FTP, SSH, HTTP and Telnet services
- Monitored live attack attempts in real time
- Captured credentials from all connection attempts

## Services Deployed
| Service | Port | Purpose |
|---------|------|---------|
| FTP | 21 | Fake file transfer server |
| SSH | 2222 | Fake secure shell server |
| Telnet | 23 | Fake remote login server |
| HTTP | 80 | Fake web server |

## Attacks Captured
| Attack | Service | Username | Password |
|--------|---------|----------|----------|
| Login attempt | Telnet | prabh | hacker |
| Login attempt | SSH | kali | pass |
| Login attempt | FTP | admin | admin123 |

## Key Finding
Every connection attempt to a honeypot is suspicious
by definition — no legitimate user has any reason to
connect to it. Zero false positives make honeypots
one of the most reliable early warning systems
available to security teams.

## What I Learned
Honeypots catch attackers who have already bypassed
perimeter defenses. In a real network a honeypot
silently logs everything — IP address, credentials
tried, timestamp — giving the SOC team full
intelligence on the attacker before they even
know they have been detected.

# Network Reconnaissance — Nmap

## Target
Metasploitable 2 — 192.168.56.101

## Tools Used
Nmap, Kali Linux

## Scans Performed
| Scan Type | Command | Purpose |
|-----------|---------|---------|
| Basic scan | nmap 192.168.56.101 | Find open ports |
| Version scan | nmap -sV 192.168.56.101 | Identify exact versions |
| Aggressive scan | nmap -A 192.168.56.101 | OS detection + scripts |
| Full port scan | nmap -p- 192.168.56.101 | All 65535 ports |

## Key Findings
| Port | Service | Version | Risk |
|------|---------|---------|------|
| 21 | FTP | vsftpd 2.3.4 | Critical |
| 139 | Samba | 3.0.20 | Critical |
| 6667 | IRC | UnrealIRCd | Critical |
| 1524 | Shell | Bindshell | Critical |
| 23 | Telnet | Linux telnetd | High |

## What I Learned
Version detection is critical — knowing vsftpd 2.3.4
specifically led directly to CVE-2011-2523 exploitation.
Every open port is a potential entry point.

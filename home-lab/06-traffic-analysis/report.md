# Traffic Analysis — Wireshark

## Target
Metasploitable 2 — 192.168.56.101

## Tools Used
Wireshark, Kali Linux

## What I Did
- Captured live network traffic between Kali and target
- Analysed Nmap scan traffic from defender perspective
- Captured FTP credentials transmitted in plain text
- Captured Telnet session including password in plain text
- Used Follow TCP Stream to reconstruct full sessions

## Key Findings
| Protocol | Encrypted | Finding |
|----------|-----------|---------|
| FTP | No | Username visible in plain text |
| Telnet | No | Password captured in plain text |
| SSH | Yes | Nothing visible — fully encrypted |
| TCP SYN | N/A | 2597 port knocks from Nmap scan |

## Critical Discovery
Telnet session reconstructed using Follow TCP Stream
showed complete login including password "msfadmin"
in plain text — visible to anyone on the network.

## What I Learned
Unencrypted protocols expose credentials to anyone
running Wireshark on the same network. SSH and SFTP
must replace Telnet and FTP in any secure environment.
2597 SYN packets from one IP in seconds is an
immediate red flag for any SOC analyst.

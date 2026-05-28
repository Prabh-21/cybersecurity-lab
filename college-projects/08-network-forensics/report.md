# Network Forensic Investigation — Packet Capture Analysis

## Tools Used
Wireshark

## What I Did
Performed forensic analysis of 6 network packet capture
files to reconstruct a full multi-stage attack.

## Attack Timeline Reconstructed
| Phase | Attack | Finding |
|-------|--------|---------|
| 1 | Reconnaissance | ARP sweep across entire subnet |
| 2 | Initial Access | RDP brute-force on two targets |
| 3 | Lateral Movement | Persistent SSH connections |
| 4 | Exfiltration | FTP brute-force — 144 attempts |
| 5 | Confirmed Breach | Successful FTP login — student/student |
| 6 | Data Theft | Plaintext credential list exfiltrated |

## Key Findings
Attacker used common credentials to gain FTP access
after 144 brute-force attempts across 12 usernames.
Full credential list exfiltrated in plaintext.

## Mitigation Recommendations
- Implement account lockout after 5 failed attempts
- Replace FTP with SFTP — encrypt all file transfers
- Deploy IDS to alert on brute-force patterns
- Enforce strong password policy across all accounts

## What I Learned
Packet captures tell the complete story of an attack.
A skilled analyst can reconstruct every step an
attacker took purely from network traffic.

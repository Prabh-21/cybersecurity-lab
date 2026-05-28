# Password Cracking — John the Ripper & Hashcat

## Target
/etc/shadow hashes from Metasploitable 2

## Tools Used
John the Ripper, Hashcat, rockyou.txt wordlist

## Method
1. Gained root access via open port 1524
2. Dumped /etc/shadow password hashes
3. Cracked hashes using dictionary attack

## Results
| Username | Password | Method |
|----------|----------|--------|
| sys | batman | John the Ripper |
| klog | 123456789 | John the Ripper |
| msfadmin | msfadmin | John the Ripper |
| postgres | postgres | John the Ripper |
| user | user | John the Ripper |
| service | service | John the Ripper |

6 out of 7 passwords cracked in under 60 seconds.

## Key Finding
All cracked passwords were either identical to the
username or simple dictionary words. This demonstrates
why password complexity policies are critical.

## What I Learned
Weak passwords are cracked instantly with dictionary
attacks. Password policies must enforce complexity,
minimum length, and prevent username as password.
rockyou.txt contains 14 million real leaked passwords —
if your password is in that list it will be cracked.

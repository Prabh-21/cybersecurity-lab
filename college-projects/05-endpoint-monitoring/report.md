# Endpoint Process Monitoring

## Target
Windows 10 workstation

## Tools Used
Sysinternals Suite (Process Explorer, Autoruns,
Process Monitor)

## What I Did
- Investigated suspicious processes running on endpoint
- Used Process Explorer to identify malicious activity
- Used Autoruns to find persistence mechanisms
- Used Process Monitor to trace file and registry activity
- Documented full investigation findings

## Key Findings
Identified suspicious processes masquerading as
legitimate Windows services. Found unauthorized
persistence mechanisms in startup registry keys.

## What I Learned
Attackers frequently hide malicious processes using
names similar to legitimate Windows processes.
Sysinternals tools are essential for any endpoint
investigation and are used daily by SOC analysts
and incident responders.

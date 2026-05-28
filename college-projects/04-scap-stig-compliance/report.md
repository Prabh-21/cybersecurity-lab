# SCAP/STIG Compliance Implementation

## Target
Windows 10 Enterprise workstation

## Tools Used
SCAP Compliance Checker, STIG Viewer, DISA STIG Benchmarks

## What I Did
- Ran initial SCAP scan to establish baseline compliance score
- Analysed all failing STIG controls in STIG Viewer
- Applied remediation for each failing control
- Re-ran SCAP scan to verify improvements
- Documented all changes made

## Results
| Metric | Before | After |
|--------|--------|-------|
| Compliance Score | 34.18% | 90.3% |
| Passing Controls | Low | High |
| Open Findings | Many | Few |

## Key Findings
Most failures were related to password policies,
audit logging settings, and unnecessary services
running by default on Windows 10.

## What I Learned
STIG compliance is a systematic process. Small
configuration changes across many controls
compound into significant security improvements.
DoD benchmarks represent best practice baselines
applicable beyond government environments.

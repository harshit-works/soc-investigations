# SOC335: CVE-2024-49138 Exploitation Investigation

**Platform:** LetsDefend · **Severity:** Medium · **Verdict:** True Positive
**MITRE ATT&CK:** T1036 Masquerading, T1068 Privilege Escalation

## Scenario
(2 sentences: what alert fired, on which host/user.)

## What I investigated
- The alert and the process involved
- The file path and file reputation (VirusTotal)
- Endpoint and log records for network activity

## Evidence
![Alert details](01-alert-details.png)
Short caption: what this shows.

![VirusTotal result](02-virustotal.png)
Short caption: what this shows.

## Timeline
| Time | Event |
|---|---|
| ... | Alert fired |
| ... | File downloaded from C2 (hxxps://...[.]com) |
| ... | Process executed |

## Finding
(3-4 sentences: why it's malicious. Wrong name (svhost.exe vs svchost.exe),
wrong location (C:\temp vs C:\Windows\System32), flagged malicious.)

## Recommendation
- Isolate the host
- Block the C2 address
- Check other hosts for contact with it
- Remove the file

## What I'd do differently
(One honest reflection.)

## Lessons learned
(Your svchost.exe lesson, in your own words.)

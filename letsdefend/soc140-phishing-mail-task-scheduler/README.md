# SOC140: Phishing Mail Detected, Suspicious Task Scheduler

![Verdict](https://img.shields.io/badge/Verdict-True%20Positive-red?style=flat-square)
![Severity](https://img.shields.io/badge/Severity-Medium-orange?style=flat-square)
![Type](https://img.shields.io/badge/Type-Phishing%20Email-blue?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-LetsDefend-lightgrey?style=flat-square)

## Summary
A mail-security alert flagged a phishing email carrying a ZIP attachment. The
email was **blocked and never delivered** to the user. I analysed the attachment
and found <what made it malicious, in one sentence>, so I classified it as a
**true positive**.

## Alert details
| Field | Value |
|---|---|
| Rule | SOC140 - Phishing Mail Detected - Suspicious Task Scheduler |
| Event ID | 82 |
| Severity | Medium |
| Type | Exchange (email) |
| Alert time | 2021-03-21T12:26:57+03:00 |
| Sender | aaronluo@cmail.carleton.ca |
| Recipient | mark@letsdefend.io |
| Delivery status | Blocked |

## Investigation
1. **Alert review:** the alert showed Phishing Mail Detected 
2. **Delivery check:** Device Action status was blocked 
3. **Attachment analysis:** 72c812cf21909a48eb9cceb9e04b865d
4. **Reputation check:** No security vendors flagged this file as malicious

## Evidence
![Alert details](01-alert-details.png)
*<what this shows>*

![Attachment analysis](02-attachment-analysis.png)
*<what this shows>*


## Why this verdict
1. ZIP looked clean on VirusTotal (0 detections), but the file inside was flagged>
2. the inner file behaves like or pretends to be something it isn't

## Why the clean ZIP score mattered
The email was blocked by the security system. The attached ZIP had 0 VirusTotal detections, but its bundled file Material.pdf was flagged by 30/61 vendors. The associated domain a.pomf.cat was flagged by 9/92 vendors. These findings indicate potentially malicious content.


## What I learned
I learned how to investigate phishing emails by checking suspicious messages, attachments, and domains using VirusTotal. I understood that a ZIP file showing zero detections can still contain suspicious files, so related indicators must also be checked. I also learned to verify whether an email was blocked or delivered, document evidence, and classify alerts as true or false positives based on the findings.


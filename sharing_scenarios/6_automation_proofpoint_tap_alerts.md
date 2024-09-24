# Scenario 6: Automation - Proofpoint TAP Alerts
### Description:
An organization is monitoring its email security and leveraging Proofpoint Targeted Attack Protection (TAP). Proofpoint TAP detects several email-based threats, including phishing attempts and malicious attachments, that were flagged as high confidence indicators of compromise (IOCs). The organization queries the TAP API to retrieve recent alerts and decides to share these threat indicators with a MISP instance to collaborate with other organizations and improve the overall threat intelligence landscape.

In this scenario, we will simulate the process of querying Proofpoint TAP for alerts and creating MISP events to share relevant indicators. The intelligence shared will include malicious email addresses, URLs, file hashes, and sender IP addresses associated with these threats.

## Attributes to Include:
- Email source

### Indicators:
We will be referencing ```misp-training/scenario_notebooks/data/proofpoint_tap.json``` for specific indicators to use for this scenario. 

## Galaxy Clusters to Include:
### Attack Pattern
 - Phishing (Spearphishing Link):
   - Technique ID: T1566.002
   - Description: Phishing email contains a link to download malware.
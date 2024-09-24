# Scenario 3: SCATTERED SPIDER Intrusion Analysis
### Description:
An organization becomes the victim of a targeted attack by the SCATTERED SPIDER threat group. The incident begins with social engineering tactics used to compromise the IT help desk and obtain credentials for initial access. Over time, the attackers escalate their privileges, establish persistence, and move laterally within the network. Eventually, BlackCat ransomware is deployed, locking down critical systems and exfiltrating sensitive customer data. The stolen data is used for extortion, threatening to release it unless a ransom is paid.

## Attributes to Include:
- Phone number used to call IT help desk
- C2 server domain and IP
- Legitimate software names and file hashes
- Malware name and file hashes
- Ransomware name and file hashes

### Indicators:
| Description                       | Category         | Type         | Value                                                            |
|-----------------------------------|------------------|--------------|------------------------------------------------------------------|
| Phishing Phone Number             | Person           | phone-number | +1-555-234-5678                                                  | 
| C2 Server Domain                  | Network activity | domain       | secure-update-check.com                                          |
| C2 Server IP Address              | Network activity | ip-dst       | 198.51.100.42                                                    |
| Legitimate Software File Name     | Network activity | filename     | AnyDesk.exe                                                      |
| Legitimate Software Hash (SHA256) | Network activity | sha256       | 6a2b5c7f8d14e3b9f5e9e1246a89e26b5e91b7120b34187dcdfb6c78f4ef5c22 |
| Malware File Name                 | Network activity | filename     | beacon.exe                                                       |
| Malware Hash (SHA256)             | Network activity | sha256       | 3e8d1c12a0f9b7e5bcb94e2ad10e53a4a3d2e2bdb4e09f2e5a8b732fbb4c9c66 |
| Ransomware File Name              | Network activity | filename     | bc_ransomware.exe                                                |
| Ransomware Hash (SHA256)          | Network activity | sha256       | b1d9b9f5f8c69e7a8b1d24c3c5d6e4b9a3c9c5f7d6e8f8b9e7f7d4c8b1e9a3f6 |


## Galaxy Clusters to Include:
### 1. Attack Pattern
 - Valid Accounts (Cloud Accounts):
   - Technique ID: T1078.004
   - Description: The attackers used valid credentials obtained through social engineering of the IT help desk to gain initial access.
 - Phishing (Spearphishing Voice):
   - Technique ID: T1566.004
   - Description: The attackers used social engineering to deceive the IT help desk into resetting credentials for initial access.
 - Remote Access Software:
   - Technique ID: T1219
   - Description: Legitimate remote access software like AnyDesk was used by the attackers to maintain persistence within the compromised environment.
 - Application Layer Protocol (Web Protocols):
   - Technique ID: T1071.001
   - Description: The attackers communicated with the C2 server using a domain (secure-update-check.com) over HTTP/HTTPS.
 - Data Encrypted for Impact
   - Technique ID: T1486
   - Description: BlackCat ransomware encrypted files on the compromised systems to deny access to key data and demand a ransom.
 - Obfuscated Files or Information
   - Technique ID: T1027
   - Description: The attackers likely used obfuscated files (e.g., Cobalt Strike beacon) to avoid detection while moving laterally in the network.

### 2. Malpedia:
 - Cobalt Strike
   - Description: Attribution to the specific malware
 - BlackCat
   - Description: Attribution to the specific ransomware

### 3. RH-ISAC Threat Actors
- SCATTERED SPIDER
  - Description: Attribution to the specific threat actor group
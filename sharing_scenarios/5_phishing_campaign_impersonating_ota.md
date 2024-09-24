# Scenario 5:  Phishing Campaign Impersonating OTA
### Description:
Fraudsters are targeting hotels in the hospitality industry by impersonating an online travel agency (OTA) to phish for credentials. The attackers send phishing emails to hotel staff, prompting them to click on a link that downloads malware. An information stealer is used to steal customer reservation data, credit card information, and other sensitive details. The fraudsters then use this stolen data to impersonate the hotel, messaging guests with an additional payment link that appears to be from the real OTA website or app.

## Attributes to Include:
- Email source 
- Email subject
- Sender IP address
- URL leading to the imposter OTA extranet login
- Malware file hashes and filename
- Impersonated OTA payment URL

### Indicators:
| Description           | Category         | Type          | Value                                                            |
|-----------------------|------------------|---------------|------------------------------------------------------------------|
| Email sender          | Payload delivery | email-src     | support@otavipservice.com                                        | 
| Email subject         | Payload delivery | email-subject | Urgent: Action Required for Your OTA Account Security            |
| Sender IP address     | Payload delivery | ip-src        | 198.51.100.56                                                    |
| Phishing URL          | Payload delivery | url           | http://secure-ota-login.com/fake-login                           |
| Malware File Name     | Network activity | filename      | ota_security_update.exe                                          |
| Malware Hash (SHA256) | Network activity | sha256        | 0f79d37dd89fe7f6dab0c5bb89ade5bcf8378cd30a960ffeeb27c08460c9bd03 |    
| Impsonated OTA URL    | Network activity | url           | http://totally-real-ota-portal.com/secure-payment                |

## Galaxy Clusters to Include:
### 1. RH-ISAC Fraud
- Booking Fraud
  - Description: A type of fraud targeting hospitality room and/or trip booking systems. Booking fraud can target customers with fraudulent opportunities or target businesses either using stolen customer credentials or demanding refunds.

### 2. Malpedia
- Vidar
  - Description: Attribution to the specific information stealer.
# Scenario 4:  Refund Fraud-as-a-Service Threat Actor Group
### Description:
The RedRefund Collective is a notorious Refund Fraud-as-a-Service group operating under a communist-themed banner. They advertise their fraudulent refund services through various platforms, including Telegram channels and specialized websites. Their services focus on defrauding retail and e-commerce companies by issuing refunds for expensive items and selling access to compromised customer accounts. They use social media platforms like Instagram, Snapchat, and TikTok for promotion, and their operations are consolidated on a Linktree page. The RedRefund Collective leverages a structured network of channels to interact with clients, manage operations, and verify successful fraud cases.

## Attributes to Include:
- Domains for fraudulent service websites
- Telegram channels for main operations, admin communications, and vouching
- Alias of a key figure in the operation
- Social media handles for Instagram, Snapchat, TikTok
- Linktree page linking all resources together

### Indicators:
| Description                   | Category         | Type      | Value                            |
|-------------------------------|------------------|-----------|----------------------------------|
| Main website                  | Network activity | domain    | redrefundcollective.com          | 
| Backup website                | Network activity | domain    | communistrefunds.net             |
| Telegram Channel (Main)       | Network activity | url       | https://t.me/redrefundcollective |
| Telegram Channel (Admin)      | Network activity | url       | https://t.me/redrefund_admins    |  
| Telegram Channel (Vouch Room) | Network activity | url       | https://t.me/redrefund_vouches   |
| Linketree URL                 | Network activity | url       | https://linktr.ee/redrefunds     |
| Contact Information (Name)    | Person           | full-name | Ivan Petrov                      |
| Instagram Handle              | Person           | text      | @redrefunds                      |
| Snapchat Handle               | Person           | text      | @refunds_commissar               |
| TikTok Handle                 | Person           | text      | @refundrevolution                |


## Galaxy Clusters to Include:
### RH-ISAC Fraud
 - Return Fraud:
   - Description: Return fraud happens when shoppers try to deceive retailers throughout the product return process to illicitly obtain a refund
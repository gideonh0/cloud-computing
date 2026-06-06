AWS has security services that map roughly to different OSI layers, though not every layer has a single dedicated AWS security product.

| No. | OSI Layer | What it protects | AWS security services / controls |
|---|---|---|---|
| 1.| **Physical** | Data center hardware, facilities | AWS global infrastructure, physical security controls, hardware lifecycle controls |
| 2.| **Data Link** | MAC, switching, local network access | Security Groups/NACLs don’t operate here exactly, but AWS network segmentation and VPC controls help; most customer-facing controls are above L2 |
| 3.| **Network** | IP routing, packet filtering | **AWS Network Firewall**, **AWS Shield** (DDoS at network/transport), **VPC route tables**, **Security Groups**, **NACLs** |
| 4.| **Transport** | TCP/UDP sessions | **AWS Shield**, **Network Firewall**, **Security Groups**, **NACLs**, **AWS Global Accelerator** for traffic steering and availability |
| 5.| **Session** | Session establishment/management | No direct AWS-only “session security” product; handled mostly by application/auth controls and load balancer/app design |
| 6.| **Presentation** | Encryption/format translation | **AWS KMS**, **AWS Certificate Manager (ACM)**, TLS/SSL on ALB/CloudFront/API Gateway |
| 7.| **Application** | HTTP/API/app logic | **AWS WAF**, **AWS Shield Advanced** (integrates with WAF), **AWS Firewall Manager**, **Amazon Cognito**, **AWS IAM**, **Amazon GuardDuty** |

## Fast mapping
- **DDoS / traffic floods** → **AWS Shield**  
- **Web attacks (SQLi, XSS, bad bots)** → **AWS WAF**  
- **Network traffic filtering** → **AWS Network Firewall**  
- **Encryption keys** → **AWS KMS**  
- **Certificates / TLS** → **AWS Certificate Manager**  
- **Identity / access control** → **AWS IAM**, **Amazon Cognito**  

---

## Exam memory trick
- **Shield = DDoS**
- **WAF = Web requests**
- **Network Firewall = Network packets**
- **KMS/ACM = Encryption**
- **IAM/Cognito = Identity**

---

AWS security is strongest when you combine **network controls (L3/L4)**, **application filtering (L7)**, **encryption (L6)**, and **identity controls** across the environment.

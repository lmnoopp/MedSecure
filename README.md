# MedSecure
Secure Medical Documentation Sending over the Private Network

## Customer Challenge
A healthcare organization requires a secure medical document processing system that ensures that all PHI data never traverses the public internet and remains completely isolated from internet-facing applications to meet HIPAA requirements.

## Solution
**MedSecure** is a **HIPAA-compliant web application** for secure medical document upload and storage. Designed for healthcare providers, MedSecure ensures **patient data remains private, encrypted, and fully isolated from the public internet.**  

<img width="696" height="935" alt="image" src="https://github.com/user-attachments/assets/f5aef746-e750-42a4-82d3-194a29bedf59" />

Built on AWS infrastructure with **Transit Gateway** and **VPC Peering**, MedSecure enables secure cross-region communication between **Virginia** and **California** while providing **centralized visibility** and **scalability** for future expansion.  

---

## Features

- **HIPAA-Compliant Document Storage**  
  Secure isolation of all uploaded documents in private VPCs, ensuring PHI never traverses the public internet.

- **Automated Redaction**  
  Uses **AWS Lambda** and **Comprehend Medical** to detect and redact sensitive patient information.
<img width="1229" height="627" alt="image" src="https://github.com/user-attachments/assets/1ecdc38c-78f8-463e-aac0-911e43dc1b07" />

- **Cross-Region Communication**  
  Low-latency, private connections between regions using **Transit Gateway** and **VPC Peering**.

- **Centralized Monitoring**  
  Full visibility into network traffic with **VPC Flow Logs**, **Athena**, and **QuickSight** dashboards.
<img width="1938" height="496" alt="image" src="https://github.com/user-attachments/assets/6d1268d6-e12e-4dee-9268-4bb201b09119" />
<img width="2000" height="476" alt="image" src="https://github.com/user-attachments/assets/7cb0064f-54e0-49f5-ad3a-6848d4526f1e" />

- **Scalable Architecture**  
  Easily expandable to new AWS regions with minimal operational overhead.

- **Provider-Friendly Portal**  
  Healthcare providers can securely upload documents from anywhere via **HTTPS-enforced CloudFront** connections.

---

## Architecture Overview

<img width="2000" height="1121" alt="image" src="https://github.com/user-attachments/assets/2278f773-0922-4b8f-bd71-3c14cd2a320f" />


- **Frontend Access**: Healthcare providers connect via VPN → CloudFront → Web Application VPC.  
- **Secure Storage**: Documents are transferred privately to Storage VPCs (one per region).  
- **Traffic Isolation**: Private endpoints ensure no internet exposure.  
- **Monitoring & Analytics**: Centralized logging and dashboards provide insights into traffic and usage.


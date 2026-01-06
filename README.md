# Scalable and Secure 3-Tier Application on AWS

This repository deploys a **highly available, scalable, and secure 3-tier architecture on AWS** using a Python Streamlit frontend, Spring Boot backend, and RDS MySQL database.  
The application is delivered via **CloudFront** and protected using **AWS WAF**, following production-grade cloud design principles.

---

## 🏗️ Architecture Overview

The application is deployed across **multiple Availability Zones**, with strict separation between public and private layers.

| Tier | Component | AWS Services | Purpose |
|-----|----------|-------------|---------|
| Edge / CDN | Global Entry Point | CloudFront, Route 53, WAF | Global delivery, HTTPS termination, DDoS & L7 protection |
| Presentation | Frontend Layer | ALB, ASG (EC2), Streamlit | Load balancing, autoscaling, user interaction |
| Application | Backend Layer | NLB, ASG (EC2), Spring Boot | API processing, internal service communication |
| Data | Database Layer | RDS MySQL | Secure, managed, highly available data storage |

---

## 🛠️ Technologies & Tools

### ☁️ Cloud & Networking
![AWS](https://img.shields.io/badge/AWS-FF9900?logo=amazonaws&logoColor=white)
![VPC](https://img.shields.io/badge/AWS_VPC-FF9900?logo=amazonaws&logoColor=white)
![ALB](https://img.shields.io/badge/Application_Load_Balancer-FF9900?logo=amazonaws&logoColor=white)
![NLB](https://img.shields.io/badge/Network_Load_Balancer-FF9900?logo=amazonaws&logoColor=white)
![Route53](https://img.shields.io/badge/Route_53-FF9900?logo=amazonaws&logoColor=white)

### 🛡️ Security & Edge
![CloudFront](https://img.shields.io/badge/CloudFront-FF9900?logo=amazonaws&logoColor=white)
![WAF](https://img.shields.io/badge/AWS_WAF-FF9900?logo=amazonaws&logoColor=white)
![IAM](https://img.shields.io/badge/IAM-FF9900?logo=amazonaws&logoColor=white)

### 🖥️ Compute & Scaling
![EC2](https://img.shields.io/badge/EC2-FF9900?logo=amazonaws&logoColor=white)
![AutoScaling](https://img.shields.io/badge/Auto_Scaling-FF9900?logo=amazonaws&logoColor=white)

### 🧩 Application Stack
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white)

### 🗄️ Database
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![RDS](https://img.shields.io/badge/Amazon_RDS-FF9900?logo=amazonaws&logoColor=white)

---

## 🔁 Request Flow

1. Users access the application via **CloudFront**, resolved through **Route 53**.
2. **AWS WAF** inspects incoming traffic.
3. Requests are forwarded to the **ALB**.
4. Frontend instances serve requests and forward API calls internally.
5. Backend traffic is routed via **NLB**.
6. Backend securely connects to **RDS MySQL** in private subnets.

---

## 🔐 Security & High Availability

- Multi-AZ deployment across all tiers  
- Public access limited to edge and frontend layers  
- Backend and database isolated in private subnets  
- WAF for Layer 7 protection  
- Auto Scaling for elasticity and resilience  
- Managed RDS for backups and availability  

---

## 📚 Documentation & Blog

- Detailed walkthrough and architecture explanation:  
  🔗 https://medium.com/@mohammedfarooq.devops

---

## 🔗 Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/farooqmohammed9)
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)](https://github.com/farooq-devops)
[![Medium](https://img.shields.io/badge/Medium-000000?logo=medium&logoColor=white)](https://medium.com/@mohammedfarooq.devops)

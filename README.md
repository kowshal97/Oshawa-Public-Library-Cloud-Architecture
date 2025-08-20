# Oshawa Public Library – Cloud Architecture 

![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Cloud](https://img.shields.io/badge/Cloud-AWS-orange)
![Architecture](https://img.shields.io/badge/Design-Microservices-blue)

This study presents the **cloud architecture design for Oshawa Public Library (OPL)** 
The architecture leverages **Amazon Web Services (AWS)** to deliver a **secure, scalable, and highly available** microservice-based web application.

---

## 📂 Deliverables
- [📥 Download Presentation (PPTX)](https://github.com/kowshal97/Oshawa-Public-Library-Cloud-Architecture/raw/main/Presentation.pptx)  
- [📥 Download Full Report (DOCX)](https://github.com/kowshal97/Oshawa-Public-Library-Cloud-Architecture/raw/main/Report.docx)  
- [📥 Download Architecture Diagram (PNG)](https://github.com/kowshal97/Oshawa-Public-Library-Cloud-Architecture/raw/main/Diagram/AWS%20Architecture%20Diagram.drawio.png)  

---

## 📌 Overview
The project delivers a **microservice-based cloud environment** for OPL with strong emphasis on:
- High Availability  
- Security  
- Scalability  
- Backup & Disaster Recovery  
- Monitoring & Logging  

---

## 🔹 Project Scope
- **Network Infrastructure**
  - Custom VPC (10.0.0.0/16)  
  - 2 Public Subnets (with Internet Gateway, NAT Gateways)  
  - 2 Private Subnets (backend + RDS)  
  - Separate route tables  

- **Compute**
  - Amazon ECS (Fargate) for containerized frontend & backend microservices  
  - Frontend in **public subnets**, Backend in **private subnets**  

- **Storage**
  - Amazon RDS for PostgreSQL (Multi-AZ, PITR enabled)  
  - Amazon S3 for media with versioning + lifecycle policy  

- **Security**
  - Security Groups (ALB, ECS, RDS isolation)  
  - IAM Roles (least privilege: S3:GetObject, PutObject, RDS connect)  
  - Encryption at rest & transit (AES-256)  

- **Scalability**
  - Auto Scaling Groups for ECS (min 2, max 4, 75% CPU threshold)  

- **Monitoring & Logging**
  - Amazon CloudWatch metrics, alarms, log collection  
  - ECS scaling triggers + RDS monitoring  

- **Backup & Recovery**
  - RDS backups with Point-in-Time Recovery (7 days)  
  - S3 versioning for object recovery  

---

## 🖼️ Architecture Diagram
[![Architecture Diagram](https://github.com/kowshal97/Oshawa-Public-Library-Cloud-Architecture/blob/main/Diagram/AWS%20Architecture%20Diagram.drawio.png)

---

## 🔗 Related Projects
- [Clinic Management Database](https://github.com/kowshal97/clinic-management-database)  
- [Online Retail Store Database](https://github.com/kowshal97/Online-Retail-Store-database)  
- [Assignment 1 – Library & College Systems](https://github.com/kowshal97/Database-design-project-)  

---

## ✍️ Notes
- Developed under the **AWS Well-Architected Framework**.  
- Built with industry best practices for **security, redundancy, and scalability**.   


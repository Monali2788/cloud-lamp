# DevOps Terraform LAMP Server

End-to-End Full Stack Application Deployment using **Terraform** and **Docker Compose**.

This project simulates a **real-world DevOps scenario** where frontend and backend code is provided by developers, and the **DevOps engineer is responsible for provisioning infrastructure and deploying the complete application stack**.

---

## 🧩 Project Overview

This repository deploys a **containerized full-stack application** on an **AWS EC2 instance** using **Terraform** for infrastructure provisioning and **Docker Compose** for application orchestration.

The stack includes:

* **React.js** – Frontend
* **Spring Boot** – Backend
* **MySQL** – Database

---

## 🏗️ Project Architecture

```
                ┌────────────────────────────┐
                │        User Browser         │
                └──────────────┬─────────────┘
                               │
                               │ HTTP :3000
                               ▼
                ┌────────────────────────────┐
                │        AWS EC2 Instance     │
                │                            │
                │  ┌──────────────────────┐ │
                │  │   React.js Container  │ │
                │  │      (Frontend)       │ │
                │  └──────────┬───────────┘ │
                │             │ REST API     │
                │             ▼               │
                │  ┌──────────────────────┐ │
                │  │ Spring Boot Container │ │
                │  │      (Backend)        │ │
                │  └──────────┬───────────┘ │
                │             │ JDBC          │
                │             ▼               │
                │  ┌──────────────────────┐ │
                │  │   MySQL Container     │ │
                │  │      (Database)       │ │
                │  └──────────────────────┘ │
                │                            │
                │   Docker Compose Runtime   │
                └────────────────────────────┘

Infrastructure Provisioned using Terraform
```

---

## 📁 Repository Structure

```
DevOps-Terraform-LAMP-Server/
├── code/                   # Frontend (React) and Backend (Spring Boot) source code
├── docker-compose.yaml     # Multi-container setup (React, Spring Boot, MySQL)
├── main.tf                 # Terraform infrastructure definition
└── README.md               # Project documentation
```

---


## ✅ Sample Terraform Output

```
Apply complete! Resources: 7 added, 0 changed, 0 destroyed.

Outputs:

App-Live =
Reactjs and Spring boot Live: http://3.16.79.49:3000

Docker-compose =
LAMP server: docker compose ps -a

MYsql-Live =
MySQL Credentials: mysql -uappuser -papppass appdb

public_ip =
Public IP address: ec2-user@3.16.79.49

sshkey =
SSH Key location: ~/.ssh/id_rsa
```

---


## 🎯 Learning Objectives

By completing this project, learners will gain hands-on experience with:

* Terraform-based infrastructure provisioning
* AWS EC2 resource management
* Docker and Docker Compose
* Deploying React + Spring Boot + MySQL
* End-to-end DevOps workflows

---



## ⭐ Final Summary

This repository provides a **complete hands-on DevOps project** demonstrating how infrastructure and applications are deployed together using Terraform and Docker Compose.

It closely mirrors real-world scenarios where DevOps engineers bridge the gap between development and production.

Happy Learning 🚀

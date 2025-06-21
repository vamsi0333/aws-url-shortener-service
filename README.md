# 🚀 AWS URL Shortener Service

A cloud-native, real-time URL shortening service with analytics tracking. Built with Python (Flask), deployed on AWS, and designed to be scalable, containerized, and CI/CD-ready.

---

## 🧩 Table of Contents

- [Motivation](#motivation)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [System Design](#system-design)
- [API Endpoints](#api-endpoints)
- [Folder Structure](#folder-structure)
- [Setup Instructions](#setup-instructions)
- [Deployment](#deployment)
- [Testing](#testing)
- [Future Improvements](#future-improvements)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [Contact](#contact)
- [License](#license)

---

## 🧠 Motivation

To build a production-style microservice that solves a common problem—link shortening and redirection—while demonstrating skills in backend development, analytics, CI/CD, and AWS. Ideal for preparing for SDE 1 roles at top tech companies.

---

## ✅ Features

- Create short, unique URLs from long links
- Track clicks: timestamp, IP address, user agent
- REST API design with Flask
- CI/CD with GitHub Actions
- AWS-hosted deployment (EKS, EC2, or Lambda)
- Future-ready with analytics and dashboard integration

---


---

## 🛠️ Tech Stack

- **Languages:** Python, Bash
- **Frameworks:** Flask, SQLAlchemy
- **Cloud:** AWS EC2, DynamoDB, Lambda, S3, EKS
- **DevOps:** Docker, GitHub Actions, Terraform or CDK
- **Data Tools:** AWS Athena, Glue, IP parsing libs

---

## 🧱 System Design

- URL records stored in DynamoDB with short code as primary key
- Analytics stored separately (DynamoDB or S3)
- Short codes generated using UUID or base62 encoding
- Stateless architecture for easy scaling via containers or Lambda
- CI/CD pushes container builds directly to AWS

---

## 📬 API Endpoints

| Method | Endpoint              | Description                        |
|--------|-----------------------|------------------------------------|
| POST   | `/shorten`            | Create short URL from long URL     |
| GET    | `/<short-code>`       | Redirect and log analytics         |
| GET    | `/analytics/<code>`   | Fetch click statistics             |

---


---

## 🧪 Setup Instructions

```bash
git clone https://github.com/your-username/aws-url-shortener-service.git
cd aws-url-shortener-service
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py

---







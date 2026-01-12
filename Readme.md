# AWS Security – Secrets Manager Web App

This project demonstrates how to **secure AWS credentials** in a Python web application using **AWS Secrets Manager**, instead of hardcoding secrets in source code.

The application is a simple FastAPI-based web app that lists Amazon S3 buckets using credentials retrieved securely at runtime.

---

## 🔐 Key Concepts Demonstrated

- Why **hardcoding AWS credentials is insecure**
- How to store secrets in **AWS Secrets Manager**
- How to retrieve secrets securely using **boto3**
- How to keep repositories safe for **public GitHub sharing**

---

## 🛠 Tech Stack

- Python 3
- FastAPI
- AWS Secrets Manager
- Amazon S3
- boto3
- Docker

---

## 📂 Project Structure

![AWS Secrets Manager Architecture](docs/workflow.png)
---

## 🧭 Architecture

The diagram below shows how the web application securely retrieves AWS credentials at runtime using AWS Secrets Manager instead of hardcoding them in source code.

![AWS Secrets Manager Architecture](docs/architecture.png)

---

## ▶️ Running the App Locally

```bash
pip install -r requirements.txt
python app.py

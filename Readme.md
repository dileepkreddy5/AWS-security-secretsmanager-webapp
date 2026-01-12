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

```text
├── app.py              # FastAPI application
├── config.py           # Retrieves credentials from Secrets Manager
├── Dockerfile          # Container configuration
├── requirements.txt    # Python dependencies
└── index.html          # Simple frontend page
---

## 🧭 Architecture

The diagram below shows how the web application securely retrieves AWS credentials at runtime using AWS Secrets Manager instead of hardcoding them in source code.

```mermaid
flowchart LR
    User[User Browser] --> App[FastAPI Web App]
    App -->|boto3 SDK| Secrets[AWS Secrets Manager]
    Secrets -->|Encrypted secrets| App
    App -->|Authenticated API Calls| S3[Amazon S3]

    subgraph AWS Cloud
        Secrets
        S3
    end

## Running the App Locally

pip install -r requirements.txt
python app.py

Open in your browser:
http://0.0.0.0:8000

#Notes

AWS credentials are not stored in the repository
Secrets are encrypted and managed via AWS Secrets Manager
This project was built as part of a guided learning lab and customized to demonstrate secure cloud development practices

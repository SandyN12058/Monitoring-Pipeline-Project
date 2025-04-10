# 🚀 Unbox Robotics DevOps Assignment

<p align="center">
  <img src="./diagrams/2-system-architecture.svg" alt="Project Architecture" width="600"/>
</p>

This project showcases a complete CI/CD and monitoring pipeline for centralized log visualization.

---

## 🧠 Tech Stack Used

| Category         | Tools / Technologies        |
|------------------|-----------------------------|
| CI/CD            | `GitHub Actions`            |
| Containerization | `Docker`, `Docker Compose`  |
| Monitoring       | `Promtail` `Loki` `Grafana` |
| Hosting          | `AWS EC2` (Ubuntu)          |
| Visualization    | `Grafana` Dashboards        |
| Logging          | Sample `logs.json` file    |

---

## 🗂️ Project Structure

![image](https://github.com/user-attachments/assets/1be568fd-09f7-4a24-ba54-0bc8a1b4b4c7)

---

## 📊 Monitoring Pipeline

- **Promtail** scrapes the `logs.txt` file
- Sends logs to **Loki**
- **Grafana** queries Loki to visualize logs in real-time

---

## 🔒 Security Best Practices Followed

- All secrets like DockerHub credentials, EC2 key, and environment variables are stored in **GitHub Secrets**
- Runtime environment variables are passed via **temporary `.env` file** (deleted after deployment)
- No hardcoding of sensitive data in any file
- SSH access to EC2 is secured via **private key in GitHub**

---

## ✅ Features Implemented

- [x] CI/CD with GitHub Actions
- [x] Docker-based containerization
- [x] EC2 deployment with Docker Compose
- [x] Loki-Promtail-Grafana log monitoring
- [x] Secure secret handling via GitHub Secrets
- [x] .env file for temporary secret injection
- [x] Architecture diagram for clarity

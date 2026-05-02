# 🚀 Jenkins Multi-Node Setup (Ubuntu + CentOS + Multi-Cloud)

This project demonstrates a **distributed Jenkins architecture** with:
- Ubuntu Master (Controller)
- Ubuntu & CentOS Agents
- Multi-cloud CI/CD setup (GCP + AWS)

---

## 🧱 Architecture Overview

### 🔹 Scenario 1: Ubuntu Master → Ubuntu Agent
- Hosted on GCP
- SSH-based agent connection
- Jobs executed on agent using labels

### 🔹 Scenario 2: Ubuntu Master → CentOS Agent
- Cross-OS Jenkins setup
- Managed package differences (`apt` vs `dnf`)
- Pipeline execution on CentOS node

### 🔹 Scenario 3: Multi-Cloud (GCP → AWS)
- Jenkins Master on GCP
- Agent on AWS EC2
- Cross-cloud job execution via SSH

---

## ⚙️ Setup Guide

### 1️⃣ Install Java

#### Ubuntu:
```bash
sudo apt update
sudo apt install openjdk-17-jdk -y
java -version

wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian binary/ > /etc/apt/sources.list.d/jenkins.list'

sudo apt update
sudo apt install jenkins -y

sudo systemctl start jenkins
sudo systemctl enable jenkins

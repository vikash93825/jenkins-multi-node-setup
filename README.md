# jenkins-multi-node-setup
Multi-node Jenkins setup with Ubuntu &amp; CentOS agents and multi-cloud (GCP + AWS) CI/CD pipeline


# 🚀 Jenkins Multi-Node Setup (Ubuntu + CentOS + Multi-Cloud)

This project demonstrates a **distributed Jenkins architecture** using:
- Ubuntu Master
- Ubuntu & CentOS Agents
- Multi-cloud setup (GCP + AWS)

---

## 🧱 Architecture Overview

### Scenario 1: Ubuntu Master → Ubuntu Agent
- Same environment (GCP)
- SSH-based agent connection

### Scenario 2: Ubuntu Master → CentOS Agent
- Cross-OS configuration
- apt vs dnf differences

### Scenario 3: Multi-Cloud (GCP → AWS)
- Jenkins Master on GCP
- Agent on AWS EC2

---

## ⚙️ Setup Steps

### 1. Install Java

#### Ubuntu:
```bash
sudo apt update
sudo apt install openjdk-17-jdk -y

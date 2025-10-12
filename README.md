<h1 align="center">🤖 RoboShop Project — Automated with Ansible 🚀</h1>

<p align="center">
  <b>End-to-end Infrastructure Automation for the RoboShop Microservices Application</b><br>
  <i>Deploy 10+ services — databases, APIs, and frontend — in one command using Ansible.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Automation-Ansible-blue?style=for-the-badge&logo=ansible" alt="Automation: Ansible Badge" />
  <img src="https://img.shields.io/badge/Language-YAML-orange?style=for-the-badge&logo=yaml" alt="Language: YAML Badge" />
  <img src="https://img.shields.io/badge/Cloud-AWS-yellow?style=for-the-badge&logo=amazonaws" alt="Cloud: AWS Badge" />
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge" alt="Status: Complete Badge" />
</p>

---

## 🧩 Overview

**RoboShop** is a **microservices-based eCommerce application** built with multiple independent services — each responsible for specific functionality (Catalogue, User, Cart, Payment, etc.).

This Ansible project automates the **installation, configuration, and deployment** of all these components — databases, backend services, and frontend — across multiple servers.

---

## ⚙️ Tech Stack

| Layer | Technology |
|:---|:---|
| **Automation** | Ansible |
| **Backend Services** | Node.js, Python, Java |
| **Databases** | MongoDB, MySQL |
| **Caching / Messaging** | Redis, RabbitMQ |
| **Frontend** | Nginx |
| **OS** | RHEL / CentOS / Amazon Linux 2 |

---



### Run Individual Components

You can test any service separately:

```bash
ansible-playbook -i inventory.ini mongo.yml
ansible-playbook -i inventory.ini payment.yml
ansible-playbook -i inventory.ini frontend.yml
```

-----

## 🧠 What Each Playbook Does

| Playbook | Purpose |
|:---|:---|
| `mongo.yml` | Installs and configures MongoDB |
| `mysql.yml` | Installs MySQL and loads schema |
| `redis.yml` | Installs Redis for caching |
| `rabbitmq.yml` | Installs RabbitMQ for messaging |
| `catalogue.yml` | Deploys Node.js Catalogue service |
| `user.yml` | Deploys User microservice |
| `cart.yml` | Deploys Cart microservice |
| `shipping.yml` | Deploys Java-based Shipping service |
| `payment.yml` | Deploys Python-based Payment service |
| `frontend.yml` | Deploys Nginx-based frontend and connects APIs |

-----

## ⚙️ Configuration Files

| File(s) | Role |
|:---|:---|
| `mongo.repo`, `rabbitmq.repo` | YUM repositories |
| `nginx.conf` | Nginx reverse proxy configuration |
| `*.service` | Systemd service files for each microservice |
| `ec2-r53.yaml` | Route53 setup (optional) |


```
```
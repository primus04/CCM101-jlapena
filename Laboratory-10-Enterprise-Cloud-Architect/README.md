
<div align="center">

# ☁️ CLOUDNOVA
### Enterprise Cloud Architect

**Virtualized • Containerized • Secured • Automated Infrastructure**

![Ubuntu](https://img.shields.io/badge/Ubuntu_Server-26.04.1-E95420?logo=ubuntu&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-29.9.2-2496ED?logo=docker&logoColor=white)
![WordPress](https://img.shields.io/badge/WordPress-CMS-21759B?logo=wordpress&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-11.4-003545?logo=mariadb&logoColor=white)
![Course](https://img.shields.io/badge/CCM101-Cloud_Computing-6C5CE7)

*An enterprise-style cloud infrastructure project built for CCM101 – Cloud Computing.*

</div>

---

## 🧭 Project at a Glance

CloudNova is a cloud infrastructure project that demonstrates how to deploy, manage, and secure a web application using **Oracle VirtualBox, Ubuntu Server, and Docker**.

The platform hosts two connected services:

- **WordPress** — website and content management
- **MariaDB** — database storage for WordPress

It also includes network configuration, firewall protection, SSH key authentication, persistent storage, and automated database backups.

| 🌐 Website | 🖥️ Server | 🐳 Containers | 🔐 Security |
|---|---|---|---|
| WordPress | Ubuntu Server | Docker Compose | UFW + SSH Keys |

---

## 🎯 Mission Objectives

- [x] Build a Linux server using Oracle VirtualBox
- [x] Configure NAT and Host-only networking
- [x] Install Docker Engine and Docker Compose
- [x] Deploy WordPress and MariaDB containers
- [x] Configure persistent volumes
- [x] Apply firewall rules and secure SSH access
- [x] Automate database backups with Bash
- [x] Schedule backups using Cron
- [x] Document deployment and maintenance procedures

---

## 🏛️ Infrastructure Blueprint

### System Architecture

```text
                  ┌─────────────────────────┐
                  │    Windows 11 Host     │
                  │   Laptop / Browser     │
                  └────────────┬────────────┘
                               │
                    Host-only Network
                    192.168.56.1 ↔ .103
                               │
                  ┌────────────▼────────────┐
                  │   Ubuntu Server VM     │
                  │   Oracle VirtualBox    │
                  │                        │
                  │       UFW / SSH        │
                  │           │            │
                  │      Docker Engine     │
                  │           │            │
                  │  ┌────────▼────────┐   │
                  │  │ cloudnova-network│   │
                  │  │                 │   │
                  │  │  WordPress      │   │
                  │  │       │         │   │
                  │  │   MariaDB       │   │
                  │  └─────────────────┘   │
                  │           │            │
                  │   Docker Volumes       │
                  │           │            │
                  │   Bash + Cron Backup  │
                  └────────────────────────┘
```

📎 **Architecture diagram:** [`architecture-diagram.png`](architecture-diagram.png)

---

## ⚙️ Technology Stack

| Layer | Technology |
|---|---|
| Host OS | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Server OS | Ubuntu Server 26.04.1 LTS |
| Container Engine | Docker Engine 29.9.2 |
| Container Management | Docker Compose 5.6.1 |
| Web Application | WordPress |
| Database | MariaDB 11.4 |
| Firewall | UFW + iptables |
| Automation | Bash + Cron |
| Remote Access | OpenSSH |
| Authentication | ED25519 SSH Key |

---

## 🌐 Network & Access

| Network / Service | Address | Role |
|---|---|---|
| NAT (`enp0s3`) | `10.0.2.15/24` | Internet connectivity |
| Host-only (`enp0s8`) | `192.168.56.103/24` | Host-to-server communication |
| Windows Adapter | `192.168.56.1` | Host-side connection |
| WordPress | `192.168.56.103:8080` | Web application |

### 🔗 Access the Website

**[🌍 Open CloudNova WordPress](http://192.168.56.103:8080)**

> The website is accessible from the Windows host when the VM and its network configuration are active.

---

## 🐳 Container Services

| Container | Image | Responsibility |
|---|---|---|
| `cloudnova-wordpress` | `wordpress:latest` | Serves the website |
| `cloudnova-database` | `mariadb:11.4` | Stores WordPress data |

Both containers communicate through the internal Docker network:

```text
cloudnova-network
```

### 💾 Persistent Storage

| Volume | Purpose |
|---|---|
| `wordpress_data` | Preserves WordPress files |
| `mariadb_data` | Preserves database files |

**Database isolation:** MariaDB is not directly exposed to the host network.

---

## 🛡️ Security Architecture

CloudNova applies layered security controls to protect the server and its services.

| Control | Configuration |
|---|---|
| Firewall | UFW enabled; incoming traffic denied by default |
| Outbound Traffic | Allowed |
| SSH Access | Restricted to Host-only network |
| SSH Password Login | Disabled |
| Root SSH Login | Disabled |
| SSH Authentication | ED25519 public-key authentication |
| Docker Access | Website access restricted to the Windows host |
| Database | Internal Docker network only |
| Credentials | Protected `.env` file excluded from GitHub |

> **Security reminder:** Never commit `.env` files, database credentials, private SSH keys, or other secrets to a public repository.

---

## 🔄 Automated Backup System

### Bash + Cron Workflow

```text
        ┌───────────────┐
        │ Cron Schedule │
        │  02:00 UTC   │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ automation-   │
        │ script.sh     │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ MariaDB Dump │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ Gzip Compress│
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ Validate File │
        └───────┬───────┘
                ▼
        ┌───────────────┐
        │ Keep 7 Days  │
        │ + Log Results│
        └───────────────┘
```

| Backup Detail | Value |
|---|---|
| Script | `automation-script.sh` |
| Directory | `/opt/cloudnova/backups/` |
| Schedule | Daily at 2:00 AM UTC |
| Philippine Time | Daily at 10:00 AM PHT |
| Compression | Gzip |
| Retention | 7 days |
| Validation | Backup file integrity check |
| Logging | Backup results recorded |

---

## 🚀 Deployment Quickstart

### 1. Enter the project directory

```bash
cd /opt/cloudnova
```

### 2. Start the services

```bash
sudo docker compose up -d
```

### 3. Verify containers

```bash
sudo docker ps
```

### 4. Check application logs

```bash
sudo docker compose logs
```

### 5. Open the website

```text
http://192.168.56.103:8080
```

📘 For complete installation, security, backup, and maintenance instructions, see the **[Operational Manual](operational-manual.md)**.

---

## 📁 Repository Layout

```text
Laboratory-10-Enterprise-Cloud-Architect/
│
├── 📄 README.md
├── 🖼️ architecture-diagram.png
├── 🐳 docker-compose.yml
├── ⚙️ automation-script.sh
├── 📘 operational-manual.md
└── 📝 final-reflection.md
```

---

## 📦 Project Deliverables

| File | Description |
|---|---|
| `architecture-diagram.png` | Infrastructure and network diagram |
| `docker-compose.yml` | WordPress and MariaDB configuration |
| `automation-script.sh` | Automated database backup script |
| `operational-manual.md` | Setup, security, and maintenance guide |
| `final-reflection.md` | CCM101 learning reflection |

---

## 💡 Key Takeaways

CloudNova brings together virtualization, containerization, networking, storage, security, and automation in one working infrastructure.

Through this project, the cloud environment demonstrates:

- **Reliable deployment** through Docker containers
- **Data persistence** through Docker volumes
- **Controlled access** through firewall and SSH configuration
- **Operational efficiency** through automated backups
- **Maintainability** through documented procedures

---

<div align="center">

### ☁️ CLOUDNOVA
*Building secure, reliable, and automated cloud infrastructure.*

**CCM101 – Cloud Computing | Laboratory 10**

</div>

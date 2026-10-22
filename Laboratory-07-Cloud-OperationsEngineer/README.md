# ☁️ Laboratory 07 - Cloud Operations Engineer

## 🎯 Mission Overview

Congratulations! Your ability to deploy multi-tier architectures has proven your technical capabilities.

You have now been promoted to the Cloud Operations Team (often referred to in the industry as Site Reliability Engineering, or SRE) at CloudNova Technologies.

Deploying a cloud application is only the first step; keeping it running smoothly is the real challenge.

When a server crashes or a web page takes ten seconds to load, you cannot simply guess what is wrong. You must rely on Observability and Monitoring to see inside your infrastructure.

Using the KillerCoda Playground, you will step into the role of a Cloud Operations Engineer. You will establish a performance baseline for your Linux server, deploy a containerized application, generate artificial web traffic, and hunt down performance metrics and system logs to prove the application is healthy.

Remember: A developer hopes the application works; a Site Reliability Engineer uses metrics and logs to prove it.

## 📌 Mission Objectives

At the end of this laboratory activity, you should be able to:

- 🖥️ Utilize native Linux command-line tools to monitor host CPU, memory, and disk capacity.
- 🐳 Deploy a web container and track its real-time performance using Docker metrics.
- 🌐 Generate web traffic and extract application access logs for analysis.
- 📝 Translate raw performance data into a readable technical report using Markdown.
- 💻 Continue expanding a professional GitHub Cloud Computing Portfolio.

## ⚙️ Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Check RAM usage. |
| `df -h /` | Check root file system storage. |
| `top` | Monitor running processes and CPU load. |
| `docker run -d --name clientwebsite -p 8080:80 nginx` | Deploy the Nginx container. |
| `curl http://localhost:8080` | Simulate a successful website request. |
| `curl http://localhost:8080/hidden-admin-page` | Generate a 404 error request. |
| `docker logs clientwebsite` | View application logs. |
| `docker ps` | Check running containers. |
| `docker stats` | Monitor real-time container resource usage. |

## 🧠 Skills Learned

- **Server Monitoring:** Learned how to check RAM, disk storage, and CPU load.
- **Docker Management:** Learned how to deploy and check a running Nginx container.
- **Traffic Simulation:** Used `curl` to send HTTP requests and generate a 404 error.
- **Log Analysis:** Learned how to identify failed requests in application logs.
- **Resource Monitoring:** Used `docker stats` to observe CPU, memory, and network usage.
- **Technical Documentation:** Practiced recording results, organizing screenshots, and writing Markdown reports.

## 📸 Screenshots

The `screenshots/` folder contains the terminal outputs collected during the laboratory activities.

- `memory-check.png`
- `disk-check.png`
- `install-nginx.png`
- `simulation1.png`
- `simulation2.png`
- `docker-logs.png`
- `container-metrics.png`

## ✅ Mission Summary

This laboratory helped me understand the importance of monitoring server health, application logs, and container resources. These skills help cloud operations engineers detect errors, troubleshoot problems, and keep applications running properly.

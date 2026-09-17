# ☁️ Mission 4: Cloud-Native Engineer

> **CloudNova Technologies | Cloud Computing Portfolio**

---

## 📌 Mission Overview

Congratulations! After successfully guiding our clients through multi-cloud evaluations, you have been promoted to the Cloud-Native Engineering Team at CloudNova Technologies.

Modern cloud computing is no longer just about renting Virtual Machines (VMs) from AWS or Azure. Today's enterprise applications are built using lightweight, portable, and lightning-fast technologies called Containers.

Your new mission is to understand the shift from traditional virtualization to containerization.

Using the KillerCoda Playground, you will step into the shoes of a Cloud-Native Engineer. You will research the differences between VMs and containers, execute your very first Docker commands, and deploy a live, containerized web server in seconds.

Remember: A traditional system administrator manages servers, but a cloud-native engineer manages the services running on them.

> 💡 **Key Idea:**  
> A traditional system administrator manages servers, while a cloud-native engineer focuses on the services and applications running on them.

---

## 🎯 Learning Objectives

At the end of this laboratory activity, you should be able to:

* Differentiate between traditional Virtual Machines (VMs) and Containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI (Command Line Interface) commands.
* Pull, run, manage, and terminate a containerized application (Nginx).
* Create professional technical documentation of container operations using Markdown.
* Continue developing a well-organized GitHub Cloud Computing Portfolio.

---

# 🐳 Docker Commands

The following commands were executed during **Checkpoints 3, 4, and 5**.

| # | Docker Command | Purpose |
|---|---|---|
| 1 | `docker version` | Displays information about the installed Docker version. |
| 2 | `docker info` | Displays details about the Docker environment. |
| 3 | `docker pull nginx` | Downloads the official Nginx image from Docker Hub. |
| 4 | `docker run -d -p 8080:80 nginx` | Creates and starts an Nginx container in detached mode and maps host port `8080` to container port `80`. |
| 5 | `curl http://localhost:8080` | Sends an HTTP request to the Nginx web server through port `8080`. |
| 6 | `docker ps` | Displays the currently running Docker containers. |
| 7 | `docker stop sharp_cohen` | Stops the running Nginx container named `sharp_cohen`. |
| 8 | `docker ps -a` | Displays both running and stopped containers to check the container status. |
| 9 | `docker rm sharp_cohen` | Removes the stopped Nginx container named `sharp_cohen`. |
| 10 | `docker ps -a` | Confirms that the removed container no longer appears in the container list. |

---

## 🧠 Skills Learned

- 🐳 Learned basic Docker commands and container management.
- 🌐 Learned how to deploy and test an Nginx container.
- 🔄 Learned the basic container lifecycle.
- 📝 Improved my Markdown documentation skills.

## ⚠️ Challenges Encountered

I initially had difficulty understanding some Docker commands and identifying the correct container name. After following the commands step by step, I was able to manage the Nginx container successfully.

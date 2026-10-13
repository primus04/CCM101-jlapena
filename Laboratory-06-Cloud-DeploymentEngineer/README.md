# ☁️ The Cloud Deployment Engineer

## 🚀 Mission Overview

Congratulations! Your flawless work in deploying data storage solutions has earned you a spot on the

**Cloud Deployment Team** at CloudNova Technologies.

Up until now, you have been deploying single containers (like a standalone web server or a storage bucket). However, real-world enterprise applications are rarely just one container. They are "multi-tier" systems that require a frontend web application communicating seamlessly with a backend database. Deploying these one by one manually is prone to error.

Enter **Docker Compose**. In this mission, you will transition from manual commands to **Infrastructure as Code (IaC)**. Using a YAML configuration file, you will define a multi-container private cloud storage application (**Nextcloud** and **MariaDB**) and deploy the entire stack simultaneously with a single command!

Remember: **A junior engineer deploys servers by typing commands; a senior engineer deploys infrastructure by writing code.**

## 🎯 Mission Objectives

At the end of this laboratory activity, you should be able to:

- 🏛️ Explain the concept of a multi-tier application architecture.
- 🧩 Understand the purpose and structure of a `docker-compose.yml` file.
- ⌨️ Use a Linux command-line text editor (`nano`) to create configuration files.
- 🚀 Deploy a multi-container application (Nextcloud + Database) using Docker Compose.
- 📖 Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
- 🌟 Continue expanding your professional GitHub Cloud Computing Portfolio.

## 💻 Commands Executed

| Command | Purpose |
|---|---|
| `mkdir nextcloud-deployment` | Creates a directory for storing the Docker Compose project files. |
| `cd nextcloud-deployment` | Moves into the deployment directory. |
| `nano docker-compose.yml` | Creates and edits the Docker Compose configuration file. |
| `docker-compose up -d` | Starts the Nextcloud and MariaDB containers in the background. |
| `docker-compose ps` | Displays the status of the running containers. |
| `docker-compose down` | Stops and removes the containers after completing the deployment. |

## 🧠 Skills Learned

- 🧰 Understanding Docker Compose for managing multiple containers.
- 🏢 Learning how multi-tier applications separate application and database responsibilities.
- 📄 Creating and managing YAML configuration files.
- 🔩 Using environment variables to configure container services.
- 🌍 Deploying and accessing a web application through a container environment.
- 📚 Documenting cloud deployment processes using Markdown and GitHub.

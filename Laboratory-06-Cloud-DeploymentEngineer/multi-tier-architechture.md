# 🏗️ Checkpoint 2 - Research: Multi-Tier Architecture

## 🌐 The Web/Application Tier

The Web/Application Tier is responsible for displaying the user interface and handling HTTP requests from users. It processes user actions and communicates with the database to retrieve or save information. It allows users to interact with the application through a web browser.

## 🗄️ The Database Tier

The Database Tier is responsible for storing and managing persistent data, such as user accounts, passwords, and other application information. It receives requests from the application tier to retrieve, add, update, or delete records. It helps keep the application's data organized and available when needed.

## 🔐 Why Separate Them?

Separating the web server and database into two containers makes the application easier to manage, maintain, and troubleshoot. It also improves security because the database can be isolated from direct public access. Additionally, each container can be updated or scaled independently without unnecessarily affecting the other service.

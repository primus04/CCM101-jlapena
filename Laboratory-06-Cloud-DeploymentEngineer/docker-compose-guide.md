# 🐳 Checkpoint 6 - Technical Documentation

## ⚙️ What Does the `services:` Block Do?

The `services:` block defines the containers that Docker Compose will create and run. In my YAML file, there are two services: `database`, which uses MariaDB to store data, and `app`, which runs Nextcloud. Docker Compose manages these services and their configurations together.

## 🔗 How Does Nextcloud Find the Database Container?

The Nextcloud container uses the `MYSQL_HOST` environment variable to find the database container. In my YAML file, `MYSQL_HOST: database` tells Nextcloud to connect to the service named `database`. Docker Compose provides network communication between the containers, allowing Nextcloud to connect to MariaDB without needing the database container's IP address.

## 🚀 Difference Between `docker run` and `docker-compose up -d`

The `docker run` command is used to create and start an individual container by specifying its image and configuration directly in the command. In contrast, `docker-compose up -d` uses a YAML file to configure and start multiple connected containers, such as Nextcloud and MariaDB, together. The `-d` option runs the containers in the background, allowing the terminal to be used for other commands.

## ✅ Conclusion

This activity helped me understand how Docker Compose connects multiple containers to build a working application. It also showed me how environment variables, service names, and YAML configuration help manage a multi-container environment.

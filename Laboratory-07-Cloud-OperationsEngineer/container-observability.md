# 📊 Container Observability Report

## 📋 1. Application Logs

**🚨 404 Error Log:**

```text
172.17.0.1 - - [22/Oct/2026:12:39:44 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

## 🔍 2. Importance of Application Logs

Application logs are important because they help cloud engineers identify errors, track user requests, and understand what happened when an application fails. They make troubleshooting easier by providing evidence that helps engineers find and fix problems quickly.

## 📈 3. Real-Time Container Metrics

- **🐳 Container Name:** `clientwebsite`
- **⚙️ CPU Usage:** [0.00%]
- **🧠 Memory Usage:** [2.727MiB]
- **💻 Command Used:** `docker stats`

## 📸 4. Screenshots

### 🐳 Docker Logs
- ![Docker Logs](screenshots/docker-logs.png)
### 📊 Container Metrics
- ![Container Metrics](screenshots/container-metrics.png)

# 📝 Mission Reflection

In this laboratory activity, I learned the importance of monitoring servers and containers to keep web applications running properly. Checking the host server's resources is important even when containers are working perfectly because the server may still have limited RAM, disk space, or CPU capacity. If these resources become insufficient, the application may become slow or stop working.

The `docker logs` command is useful when a user cannot log in to a web application because it allows us to check the application's recorded activities and errors. By examining the logs, we can look for failed requests, error messages, or other problems that may explain why the login process is not working. This helps us find the cause instead of guessing.

Monitoring logs and metrics have different purposes. Logs show specific events and provide details about what happened, such as a failed request or a 404 error. Metrics show numerical measurements, such as CPU usage, memory consumption, and network activity. Both are important because logs help identify errors while metrics help us understand the application's overall performance.

Large enterprise companies can monitor thousands of containers using tools such as Prometheus and Grafana. Prometheus collects and stores monitoring metrics, while Grafana displays the information through dashboards and graphs. These tools help engineers monitor many systems and identify performance problems more efficiently.

Finally, this laboratory improved my ability to troubleshoot Linux environments. I learned how to check system resources, deploy an Nginx container, generate web traffic using `curl`, examine application logs, and monitor container performance using `docker stats`. I also learned that troubleshooting requires collecting evidence and understanding the results before deciding how to fix a problem. These skills will help me become a better cloud operations engineer.

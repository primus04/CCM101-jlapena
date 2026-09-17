# ☁️ Mission: Mission Reflection

This mission helped me understand the difference between using Docker containers and Virtual Machines. A Docker container starts much faster because it does not need to install or boot a complete operating system. In comparison, setting up a Virtual Machine requires installing an operating system, which takes more time and uses more resources. This made me see why containers are useful for quickly deploying applications.

Port mapping such as `-p 8080:80` is necessary because it connects a port on the host machine to a port inside the container. In our activity, port `8080` allowed us to access the Nginx web server running on port `80` inside the container. Without port mapping, the web server would not be directly accessible from the host through that port.

When the `docker rm` command is used, the container itself and the data stored inside its writable layer are removed. This means that important data should be stored using volumes or another external storage method if it needs to remain after the container is deleted.

Containerization also changes how developers and IT operations teams work together. Developers can package an application with its dependencies, while IT teams can deploy the same container in different environments. This makes deployment more consistent and supports better teamwork in a DevOps environment.

My GitHub portfolio is also evolving as I add more cloud computing activities and documentation. I am learning how to organize my projects, document commands, and explain what I learned from each activity. Overall, this mission gave me practical experience with Docker and helped me understand how containerization can improve modern software development and IT operations.

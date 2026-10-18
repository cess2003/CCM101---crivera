# Mission Reflection

**1. Boot time and setup compared to a VM.**
A Docker container started in just a few seconds, while a Virtual Machine needs a full operating system installation and a boot process that can take many minutes. With Docker, I only needed to pull the Nginx image and run one command. Installing and configuring Nginx on a VM would have required installing the OS, updating packages, installing the web server and configuring it manually.

**2. Why port mapping is necessary.**
A container has its own isolated network, so the web server listening on port 80 inside it is not reachable from outside by default. Using `-p 8080:80` connects port 8080 on the host to port 80 in the container, allowing me to access Nginx through `localhost:8080`. Without it, the server would run but nobody could reach it.

**3. What happens to data after `docker rm`.**
When a container is removed with `docker rm`, its writable layer is deleted together with any data stored inside it. That is why important data must be stored in volumes, which exist separately from the container and survive its removal.

**4. Containers and DevOps.**
Containers reduce the "it works on my machine" problem because developers package the application with all its dependencies, and operations teams run that exact same package in production. This makes deployments faster, more consistent and easier to automate, and it encourages both teams to collaborate through shared tools such as Dockerfiles and CI/CD pipelines.

**5. How my portfolio is evolving.**
My GitHub portfolio has grown from simple cloud comparisons to hands-on technical work with real commands, screenshots and documentation. Each lab adds a new skill, and the repository now shows a clear progression from cloud concepts toward real container deployment. It is becoming a record of what I can actually do, not only what I have studied.

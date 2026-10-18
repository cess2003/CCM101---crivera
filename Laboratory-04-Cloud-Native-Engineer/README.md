Laboratory 04: The Cloud-Native Engineer

Mission Overview

In this mission, I assumed the role of a Cloud-Native Engineer at CloudNova Technologies. I conducted a comparative analysis of Virtual Machines and Containers, and subsequently utilized a KillerCoda Docker environment to deploy and manage a containerized Nginx web server.

Objectives

* Differentiate between Virtual Machines and Containers
* Access a Docker-enabled environment using KillerCoda
* Execute fundamental Docker CLI commands
* Pull, run, manage and terminate an Nginx container
* Document container operations using Markdown
* Continue developing my GitHub-based Cloud Computing Portfolio

Docker Commands Executed

Checkpoint 3

* docker --version
* docker version
* docker info

Checkpoint 4

* docker pull nginx
* docker run -d --name my-nginx -p 8080:80 nginx
* curl http://localhost:8080

Checkpoint 5

* docker ps
* docker stop my-nginx
* docker ps -a
* docker rm my-nginx

Skills Learned

* Explaining the architectural differences between VMs and containers
* Pulling images and running containers in detached mode
* Mapping ports between host and container
* Managing the container lifecycle (run, stop, remove)
* Writing technical documentation in Markdown

## Challenges Encountered
- **Understanding port mapping:** At first I was confused about why `-p 8080:80` uses two different port numbers. I learned that the first number is the port on the host and the second is the port inside the container, so `curl http://localhost:8080` reaches Nginx on port 80 in the container.
- **Remembering the order of the lifecycle commands:** I had to stop the container before I could remove it with `docker rm`. Using `docker ps -a` helped me see stopped containers that no longer appear in `docker ps`.
- **Slow KillerCoda environment:** The playground took a moment to load, and the terminal sometimes responded slowly. I waited until the environment was fully ready before running the Docker commands.
- **Taking and uploading screenshots:** Saving the screenshots with the exact file names (`docker-version.png`, `nginx-running.png`, `container-lifecycle.png`) and uploading them to the `screenshots` folder on GitHub required extra care so that the images displayed correctly in the README.
- **Writing Markdown tables:** Aligning the columns and separators in the comparison table took a few tries before it rendered properly on GitHub.

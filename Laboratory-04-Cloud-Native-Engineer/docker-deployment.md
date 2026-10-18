# Docker Deployment: Nginx Container Lifecycle

| Command | What it did |
|---|---|
| `docker ps` | Listed all running containers, showing my `my-nginx` container with its ID, image, status and port mapping. |
| `docker stop my-nginx` | Gracefully stopped the running Nginx container. |
| `docker ps -a` | Listed all containers including stopped ones, confirming that `my-nginx` showed an "Exited" status. |
| `docker rm my-nginx` | Permanently removed the stopped container from the system. |
| `docker ps -a` | Confirmed that `my-nginx` no longer appears in the list. |

## Deployment Commands

```bash
docker pull nginx
docker run -d --name my-nginx -p 8080:80 nginx
curl http://localhost:8080
```

- `docker pull nginx` downloads the official Nginx image from Docker Hub.
- `-d` runs the container in detached (background) mode.
- `--name my-nginx` gives the container a readable name.
- `-p 8080:80` maps port 8080 on the host to port 80 in the container.

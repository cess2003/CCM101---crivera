# Technical Documentation: Docker Compose

## What does the `services:` block do?
The `services:` block defines the individual container workloads that make up the multi-container application. Each service listed under this block represents a distinct container instance (in this case, `database` and `app`), along with its specific configurations such as Docker images, environment variables, and network port mappings.

## Service Discovery (`MYSQL_HOST`)
The Nextcloud app container locates the MariaDB database container through Docker Compose's built-in internal DNS networking. By setting `MYSQL_HOST=database`, Docker automatically resolves the service name `database` to the private container IP address assigned to MariaDB, eliminating the need to hardcode dynamic IP addresses.

## `docker run` vs. `docker-compose up -d`
* **`docker run`**: Used to manage single container instances manually via long CLI commands. If an application requires multiple linked containers, you must run multiple sequential commands and configure network links manually.
* **`docker-compose up -d`**: Uses Infrastructure as Code (IaC) to build, link, and deploy multi-container stacks in the background using a single command based on a declarative YAML file.

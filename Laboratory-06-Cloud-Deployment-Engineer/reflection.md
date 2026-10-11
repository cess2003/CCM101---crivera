# Mission Reflection

Writing a `docker-compose.yml` file completely changes how cloud engineering feels compared to typing individual terminal commands. Instead of relying on memory or bash history to run multiple complex `docker run` flags, Compose lets you write down your whole setup as code. It makes deployments consistent, reproducible, and easy to share across teams without missing steps.

Working with YAML definitely requires attention to detail, especially with spacing. If you accidentally use tabs instead of spaces or mess up the indentation, YAML parsers fail immediately with syntax errors. Since structure in YAML defines how variables and blocks relate to each other, an indentation mistake breaks the whole configuration.

Using environment variables like `MYSQL_PASSWORD` in the Compose file kept configuration dynamic and simplified how containers talk to each other. Instead of hardcoding settings into individual container images, variables allow us to adjust database credentials or hostnames seamlessly across development and production setups.

Deploying a multi-container suite like Nextcloud and MariaDB in under two minutes felt fast and efficient. Seeing a full-fledged cloud storage platform run instantly with just `docker-compose up -d` highlighted how powerful containers are.

Looking back at Mission 1, my understanding of cloud infrastructure has grown significantly. I started out just learning basic cloud terms and individual container commands, but now I’m treating infrastructure like actual software code that can be version-controlled, deployed, and torn down cleanly in seconds.

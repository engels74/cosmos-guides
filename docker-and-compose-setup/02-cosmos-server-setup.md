# 02) Cosmos Server setup

Now we will install Cosmos Server. It's fairly straightforward. You can do it in two ways: the traditional Docker way or with a Docker Compose file.

In this tutorial, I'll be using Docker Compose.

### Using Docker Compose

1. To make it easier to use `docker compose`, I always start by creating a new directory for all of my docker compose containers:

```bash
sudo mkdir -p /opt/docker-all && sudo chown -R $USER:$USER /opt/docker-all
```

2. Then we'll make a `docker-compose.yml` file that contains our Docker Compose containers:

```bash
nano /opt/docker-all/docker-compose.yml
```

3. Then we should fill in the Docker Compose service/container for Cosmos Server. It looks like this:

```yaml
version: "3.9"
services:
  cosmos-server:
    container_name: cosmos-server
    image: azukaar/cosmos-server:latest
    environment:
      - TZ=UTC ## https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - "/var/run/docker.sock:/var/run/docker.sock"
      - "/var/lib/cosmos:/config"
      - "/:/mnt/host"
    hostname: cosmos-server
    privileged: true
    restart: unless-stopped
```

4. To close the file, use `CTRL-X`, press `Y` and then press `ENTER` to save the file in Nano.
5. The whole process should look like this:\
   [![asciicast](https://asciinema.org/a/kwnAROU8fAvcKHKGwS7go02hG.svg)](https://asciinema.org/a/kwnAROU8fAvcKHKGwS7go02hG)

### On to the next step!

# 02) Cosmos Server setup

Now we will install Cosmos Server. Previously, you could use Docker Compose to launch and use Cosmos Server. But since the release of Cosmos Server v0.14.x, this is not supported any longer.



### Preparing Docker Compose for later

We're going to create a folder for later use.

1. To make it easier to use `docker compose`, I always start by creating a new directory for all of my docker compose containers:

```bash
sudo mkdir -p /opt/docker-all && sudo chown -R $USER:$USER /opt/docker-all
```

### Installing Cosmos Server

Installing Cosmos Server is very simple. All you need is to run this command, and Docker will take care of the rest.

1. Run the following command:

```bash
docker run -d --network host  --privileged --name cosmos-server -h cosmos-server --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v /:/mnt/host -v /var/lib/cosmos:/config azukaar/cosmos-server:latest
```

2. The process should look like this:

[![asciicast](https://asciinema.org/a/tUNwrwP3rmGGADQjOIeQWEkcm.svg)](https://asciinema.org/a/tUNwrwP3rmGGADQjOIeQWEkcm)

### On to the next step!

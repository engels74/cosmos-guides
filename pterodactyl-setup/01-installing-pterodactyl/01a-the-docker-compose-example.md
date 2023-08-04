# 01a) The Docker Compose example

### The Docker Compose Example

1. To install Pterodactyl, you should use the `docker-compose.pt.yml` example that I made. It's just a bundled version of the official Pterodactyl Docker images. It includes both the Panel and Wings in one docker-compose file.
2. First, we need to create the `docker-compose.pt.yml` example. I'm going to put mine in this directory, since this is what I created back in the [beginning of this guide](../../docker-and-compose-setup/02-cosmos-server-setup.md).

```bash
nano /opt/docker-all/docker-compose.pt.yml
```

3. You should use this `docker-compose.pt.yml` example, but remember to edit out the parts, that says `!!! CHANGE ME !!!` or something similar.

{% hint style="warning" %}
**Remember** to also change the `APP_URL`.\
In my case, the subdomain `pterodactyl.engels.zip` is used. For the sake of simplicity, I recommend you keep the `pterodactyl` as your subdomain.
{% endhint %}

```yaml
version: "3.9"
x-common:
  pt-database: &db-environment
    # Do not remove the "&db-password" from the end of the line below, it is important
    # for Panel functionality.
    MYSQL_PASSWORD: &db-password "!!Change This To Your Own Password!!"
    MYSQL_ROOT_PASSWORD: "!!Change This To A Different Password!!"
  pt-panel: &panel-environment
    APP_URL: "https://pterodactyl.ChangeThisToYourDomain.com"
    # A list of valid timezones can be found here: http://php.net/manual/en/timezones.php
    APP_TIMEZONE: "Europe/Berlin"
    APP_SERVICE_AUTHOR: "your@email.com"
    # Uncomment the line below and set to a non-empty value if you want to use Let's Encrypt
    # to generate an SSL certificate for the Panel.
    # LE_EMAIL: ""
  mail: &mail-environment
    MAIL_FROM: "your@email.com"
    MAIL_DRIVER: "smtp"
    MAIL_HOST: "mail"
    MAIL_PORT: "1025"
    MAIL_USERNAME: "your@email.com"
    MAIL_PASSWORD: "!!Change This To Another Different Password!!"
    MAIL_ENCRYPTION: "true"

#
# ------------------------------------------------------------------------------------------
# DANGER ZONE BELOW
#
# The remainder of this file likely does not need to be changed. Please only make modifications
# below if you understand what you are doing.
#
services:
  pt-database:
    container_name: pt-database
    image: mariadb:10.5
    labels:
      - "cosmos-force-network-secured=true"
      - "cosmos-auto-update=true"
    command: --default-authentication-plugin=mysql_native_password
    volumes:
      - "/srv/pterodactyl/database:/var/lib/mysql"
    environment:
      <<: *db-environment
      MYSQL_DATABASE: "panel" # Don't change this
      MYSQL_USER: "pterodactyl" # Don't change this
      TZ: "Europe/Berlin" # You can change this to your timezone
    restart: unless-stopped

  pt-redis:
    container_name: pt-redis
    image: "redis:alpine"
    labels:
      - "cosmos-force-network-secured=true"
      - "cosmos-auto-update=true"
    environment:
      TZ: "Europe/Berlin" # You can change this to your timezone
    ports:
      - 6379:6379
    volumes:
      - /srv/pterodactyl/redis:/data
    command: redis-server --save 20 1 --loglevel warning
    restart: unless-stopped

  pt-panel:
    container_name: pt-panel
    image: ghcr.io/pterodactyl/panel:latest
    labels:
      - "cosmos-force-network-secured=true"
      - "cosmos-auto-update=true"
    ports:
      - "10080:80"
      - "10443:443"
    links:
      - pt-redis
      - pt-database
    volumes:
      - "/srv/pterodactyl/var:/app/var" # Don't change this
      - "/srv/pterodactyl/nginx:/etc/nginx/http.d" # Don't change this
      - "/srv/pterodactyl/certs:/etc/letsencrypt" # Don't change this
      - "/srv/pterodactyl/logs:/app/storage/logs" # Don't change this
    environment:
      <<: [*panel-environment, *mail-environment]
      DB_PASSWORD: *db-password
      APP_ENV: "production" # Don't change this
      APP_ENVIRONMENT_ONLY: "false" # Don't change this
      CACHE_DRIVER: "redis" # Don't change this
      SESSION_DRIVER: "redis" # Don't change this
      QUEUE_DRIVER: "redis" # Don't change this
      REDIS_HOST: "pt-redis" # Don't change this
      DB_HOST: "pt-database" # Don't change this
      DB_PORT: "3306" # Don't change this
      TZ: "Europe/Berlin" # You can change this to your timezone
    restart: unless-stopped

  pt-wings:
    container_name: pt-wings
    image: ghcr.io/pterodactyl/wings:latest
    labels:
      - "cosmos-auto-update=true"
    ports:
      - "8080:8080"
      - "2022:2022"
    tty: true
    environment:
      TZ: "Europe/Berlin" # You can change this to your timezone
      WINGS_UID: 988
      WINGS_GID: 988
      WINGS_USERNAME: pterodactyl
    volumes:
      - "/var/run/docker.sock:/var/run/docker.sock" # Don't change this
      - "/var/lib/docker/containers:/var/lib/docker/containers" # Don't change this
      - "/etc/pterodactyl:/etc/pterodactyl" # Don't change this
      - "/var/lib/pterodactyl:/var/lib/pterodactyl" # Don't change this
      - "/var/log/pterodactyl:/var/log/pterodactyl" # Don't change this
      - "/tmp/pterodactyl:/tmp/pterodactyl" # Don't change this
      - "/etc/ssl/certs:/etc/ssl/certs:ro" # Don't change this
    network_mode: "bridge"
    restart: unless-stopped

```

4. To close the file, use `CTRL-X`, press `Y` and then press `ENTER` to save the file in Nano.
5. The whole process should look like this:

[![asciicast](https://asciinema.org/a/2Ybj5JI4Nf2vMWA1I6P8v3cr0.svg)](https://asciinema.org/a/2Ybj5JI4Nf2vMWA1I6P8v3cr0)

### On to the next step!

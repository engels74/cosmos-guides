# 01c) Launching Pterodactyl

### Launching Pterodactyl

1. To launch the `docker-compose.pt.yml` we just created, simply just run this command:

```bash
docker compose -f /opt/docker-all/docker-compose.pt.yml up -d
```

2. This will activate all Pterodactyl services at once

[![asciicast](https://asciinema.org/a/z9c20xJNQQTJkHBBgiOHecrR5.svg)](https://asciinema.org/a/z9c20xJNQQTJkHBBgiOHecrR5)

3. We'll need to do a few things, before we continue with the installation.
4. First of all, you should **Stop** the `pt-wings` container, since it'll keep restarting over and over for now.
5. You can find the `pt-wings` container inside the `pt-stack` .

<figure><img src="https://i.imgur.com/8TNwKG8.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

---
description: Making everything slightly easier
---

# 01a) Creating a network for Pterodactyl

So to ease up the installation process, and make Cosmos act nicely with our Pterodactyl panel, database, cache, and wings. We'll create a network for all Pterodactyl parts to connect to. This should make the installation a bit easier.

### Creating a Docker network

1. Create a bridge network in Docker by running this command. This will create a `bridge` network named `cosmos-pt-all` .&#x20;

```bash
docker network create cosmos-pt-all
```

2. You can see if the network has been created with:

```bash
docker network -ls
```

3. The `cosmos-pt-all` network should show up on the list.
4. From a console point of view, it should simply look like this:

[![asciicast](https://asciinema.org/a/lkciJpNyCsAEjunl9cIW5SDYj.svg)](https://asciinema.org/a/lkciJpNyCsAEjunl9cIW5SDYj)

5. Done! Let's continue.

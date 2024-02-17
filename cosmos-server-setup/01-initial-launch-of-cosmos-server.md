# 01) Initial launch of Cosmos Server

### Finding your Public IPv4

1. We should first obtain your Public IPv4 address of your server. You can accomplish this by issuing the following command:

```bash
curl -4 icanhazip.com
```

2. This will output your Public IPv4, which we will need when we first set up Cosmos Server.

### Checking if Cosmos Server is running

1. In the previous installation step, we ran the `docker run` command, which automatically started Cosmos Server.
2. It should therefore already be running. You can confirm this by running:

```bash
docker ps -a
```

3. The output should show Cosmos Server running:

```bash
CONTAINER ID   IMAGE                          COMMAND                  CREATED         STATUS         PORTS     NAMES
cb1e2031f830   azukaar/cosmos-server:latest   "sh -c './$(cat /bin…"   2 minutes ago   Up 2 minutes             cosmos-server
```

4. From a console point of view, it should simply look like this:

[![asciicast](https://asciinema.org/a/KMmyTt87vuPk0JKwoTBzboGvS.svg)](https://asciinema.org/a/KMmyTt87vuPk0JKwoTBzboGvS)

### Heading into Cosmos

1. Enter your public IPv4 + port "80" into your browser to access your Cosmos instance. In my case, it looks like this:

```bash
89.33.85.247:80
```

2. When you visit your URL, it should look like this:

<figure><img src="https://i.imgur.com/acDhkMR.png" alt="" width="563"><figcaption></figcaption></figure>

6. Yay! Now we're ready to continue!

### On to the next step!

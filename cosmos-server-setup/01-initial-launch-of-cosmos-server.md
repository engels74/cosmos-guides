# 01) Initial launch of Cosmos Server

### Finding your Public IPv4

1. We should first obtain your Public IPv4 address of your server. You can accomplish this by issuing the following command:

```bash
curl -4 icanhazip.com
```

2. This will output your Public IPv4, which we will need when we first set up Cosmos Server.

### Heading into Cosmos

1. Now we should run `dcup`, which will start our Cosmos Server.
2. If, for some reason, the `dcup` fails, you can run the command manually, using

```bash
docker compose -f /opt/docker-all/docker-compose.yml up -d
```

3. Enter your public IPv4 + port "80" into your browser to access your Cosmos instance. In my case, it looks like this:

```bash
89.33.85.247:80
```

4. From a console point of view, it should look like this:

[![asciicast](https://asciinema.org/a/65zp6Cgng1KT45WGbwIZBhkQd.svg)](https://asciinema.org/a/65zp6Cgng1KT45WGbwIZBhkQd)

5. When you visit your URL, it should look like this:

<figure><img src="https://i.imgur.com/acDhkMR.png" alt="" width="563"><figcaption></figcaption></figure>

6. Yay! Now we're ready to continue!

### On to the next step!

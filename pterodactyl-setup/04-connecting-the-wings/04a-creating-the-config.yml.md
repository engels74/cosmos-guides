# 04a) Creating the config.yml

For this section, we'll create a proper 'config.yml' file for our 'pt-wings' container. Fortunately, the Pterodactyl Panel does the majority of the legwork for us. We only need to make a minor change because the default ports it wants to use for game servers are usually already in use by Docker or other Docker containers.

### Creating the config file

1. Head to the **Configuration** tab of your newly created Node: <img src="https://i.imgur.com/8xMPzIi.png" alt="" data-size="line">
2. This will contain your node's unique `config.yml` file. This is required for the `pt-wings` to function properly and to communicate with the Panel.
3. In my case, it looks like this:

```yaml
debug: false
uuid: 89383819-4343-4978-b335-07d99252bb8f
token_id: CILwtxlbX2Zz9FPO
token: fq7gZYyMAaXlfZhdmZtZpaBUxCgbjXzcFL82TRJeZuZlQ3H9PYfFXmM6NrAehyWS
api:
  host: 0.0.0.0
  port: 443
  ssl:
    enabled: false
    cert: /etc/letsencrypt/live/pterodactylnode.engels.zip/fullchain.pem
    key: /etc/letsencrypt/live/pterodactylnode.engels.zip/privkey.pem
  upload_limit: 100
system:
  data: /var/lib/pterodactyl/volumes
  sftp:
    bind_port: 2022
allowed_mounts: []
remote: 'https://pterodactyl.engels.zip'
```

{% hint style="warning" %}
**Do not** copy this specific text example to your `config.yml` - it'll not work.\
You need to use the text from _your_ panel!
{% endhint %}

4. Copy the `config.yml` into your text-editor of your choice.
5. At the bottom, below the `remote:` part, you need to add this:

```yaml
docker:
  network:
    interface: 172.41.0.1
    name: pterodactyl_nw
    ispn: false
    driver: bridge
    network_mode: pterodactyl_nw
    is_internal: false
    enable_icc: true
    interfaces:
      v4:
        subnet: 172.41.0.0/16
        gateway: 172.41.0.1
allowed_origins:
- 'yourPanelDomainHere.domain.com'
```

This will cause the `pt-wings` to create a new network called `pterodactyl_nw`, which will be used by all game servers. It also uses a port range that is quite different from what Docker uses by default.

{% hint style="warning" %}
**Remember** to change the `allowed_origins` URL, to the URL of your panel!\
In my case, I would enter `pterodactyl.engels.zip` **without** `http` or `https`.
{% endhint %}

6. In my case, after I added the extra text, my `config.yml` will look like this:

```yaml
debug: false
uuid: 89383819-4343-4978-b335-07d99252bb8f
token_id: CILwtxlbX2Zz9FPO
token: fq7gZYyMAaXlfZhdmZtZpaBUxCgbjXzcFL82TRJeZuZlQ3H9PYfFXmM6NrAehyWS
api:
  host: 0.0.0.0
  port: 443
  ssl:
    enabled: false
    cert: /etc/letsencrypt/live/pterodactylnode.engels.zip/fullchain.pem
    key: /etc/letsencrypt/live/pterodactylnode.engels.zip/privkey.pem
  upload_limit: 100
system:
  data: /var/lib/pterodactyl/volumes
  sftp:
    bind_port: 2022
allowed_mounts: []
remote: 'https://pterodactyl.engels.zip'
docker:
  network:
    interface: 172.41.0.1
    name: pterodactyl_nw
    ispn: false
    driver: bridge
    network_mode: pterodactyl_nw
    is_internal: false
    enable_icc: true
    interfaces:
      v4:
        subnet: 172.41.0.0/16
        gateway: 172.41.0.1
allowed_origins:
- 'pterodactyl.engels.zip'
```

### Saving the `config.yml` the right way

1. To get this file onto the server, place it in the `/etc/pterodactyl` directory as the root user, or with `sudo`.
2. To achieve this, I'll simply just use Nano and paste the text in there. Use this command:

```bash
sudo nano /etc/pterodactyl/config.yml
```

3. Paste the text into the terminal, press `CTRL-X` to finish editing, then `Y` to confirm and `ENTER` to save.
4. Looks like this from a terminal point of view:

[![asciicast](https://asciinema.org/a/Qd6pOyiqrjgZ6TcaPypJvaQQd.svg)](https://asciinema.org/a/Qd6pOyiqrjgZ6TcaPypJvaQQd)

5. Now we can continue to the next step :thumbsup:

### GIF Guide

<figure><img src="https://i.imgur.com/4aEubLF.gif" alt=""><figcaption><p>Hopefully this helps, if you're confused about the process :)</p></figcaption></figure>

### On to the next step!

# 01c) Isolating networks

### Isolating Networks

1. To effectively isolate the containers, we must disconnect the `pt-panel`, `pt-database`, and `pt-redis` from the `docker-all_default` network.
2. This is accomplished by going into `Details` of each individual container, then navigating to the `Network` menu, selecting the `docker-all_default` network, and pressing the `Disconnect` button.

<figure><img src="https://i.imgur.com/TBBiRPR.png" alt=""><figcaption></figcaption></figure>

3. To ensure that the containers run in `bridge` mode from now on, we need modify the "Network Mode" to `bridge` rather than `docker-all_default`. This is accomplished at the top of the Network menu:

<figure><img src="https://i.imgur.com/ZdPUcFd.gif" alt=""><figcaption></figcaption></figure>

4. This has to be done on both the `pt-panel`, `pt-database` and the `pt-redis` containers. The `pt-wings` is already running in bridge.
5. I tried making the containers run on `network_mode: bridge` in the docker compose example, but that didn't work out, since the `pt-redis` container kept acting strangely.

### Linking containers

1. While we are in the Network menu, we also need to connect the `pt-database` and the `pt-redis` containers to the same network as the `pt-panel`.
2. In my case, the network name for my `pt-panel` is `cosmos-network-KPSZc1hIU`.

<figure><img src="https://i.imgur.com/rBCxArb.png" alt="" width="375"><figcaption></figcaption></figure>

3. I'll find my `cosmos-network-KPSZc1hIU` network in the `Network` tab of `pt-database` and `pt-redis` and connect the containers to it:

<figure><img src="https://i.imgur.com/1Zxj2nY.gif" alt=""><figcaption></figcaption></figure>

4. The final look of all the Pterodactyl containers should be something like this:

<figure><img src="https://i.imgur.com/ytvxCmO.png" alt=""><figcaption></figcaption></figure>

5. You should restart the `pt-panel` container after all this is done, so it can reconnect properly to the `pt-database` and `pt-redis` containers.

<figure><img src="https://i.imgur.com/KYSciai.png" alt="" width="375"><figcaption></figcaption></figure>

###

### Check if the `pt-panel` is running properly

1. To check if the `pt-panel` works as intended, it should contain these last lines in the log:

```log
2023-07-25 22:21:38 Starting cron jobs.
2023-07-25 22:21:38 Starting supervisord.
2023-07-25 22:21:38,846 CRIT Server 'unix_http_server' running without any HTTP authentication checking
```

2. This means the server is now running, and we can continue with creating reverse proxied URLs.

##

### GIF Guide

Here's how the whole process _should_ look, including:

* Disconnecting the containers from the `docker-all_default` network
* Linking the `pt-database` & `pt-redis` containers to the network of `pt-panel`
* Updating the network mode to `bridge`
* Restarting the `pt-panel` container.

<figure><img src="https://i.imgur.com/6hKkveS.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

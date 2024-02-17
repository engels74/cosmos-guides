# 03c) Setting up the node

In this section, we will set up the node for the first time. First and foremost, we must create the node using the Panel. When the node is created, it will provide us with a 'config.yml' template to use for our actual 'pt-wings' container.

Don't worry if it sounds complicated; I'll walk you through the process.

### Setting up the node

1. Head to the **Nodes** menu in the Panel web UI: <img src="https://i.imgur.com/DA0eD2x.png" alt="" data-size="line">
2. Select the **Create New** button: <img src="https://i.imgur.com/NVqOvgO.png" alt="" data-size="line">
3. Again, you are free to name it whatever you want. In my case, I'll simply call it `EuVPSNode01`.
4. You can leave the **Description** field blank or fill it with whatever information you think is necessary.
5. The **Location** should be set to the one you [just created](03b-setting-up-a-location.md).
6. The **Node Visibility** should be set to **Public** (at least for now).
7. Set the **FQDN** to the reverse proxied URL we created for the `pt-wings` container. That would be `pt-wings.engels.zip` in my case.
8. For the **Communicate Over SSL**, set it to **Use SSL Connection**.
9. For the **Behind Proxy**, set it to **Behind Proxy**.
10. The **Daemon Server File Directory** should be left at its default value of `/var/lib/pterodactyl/volumes`. This is where all of the game server data will be stored, in separate folders. This is set in the [docker compose example](../01-installing-pterodactyl/01a-the-docker-compose-example.md).
11. The **Total Memory** setting should be set to the total amount of RAM you want to dedicate to game servers. This can be changed later, so don't be concerned if you set it too high or too low. Because I'm using a low-cost VPS with 8GB of RAM total, I'll go with 4GB, which is 4096MB.
12. The **Memory Over-Allocation** percentage is the percentage by which you will allow the Total Memory limit to be exceeded. I'm going to set mine at 0%.
13. The **Total Disk Space** should be set to the amount of disk space you want to dedicate to your game servers. This can also be changed later, so don't be concerned if it's too high or too low. I'm going to set mine to 20GB, which is 20480MB.
14. The **Disk Over-Allocation** percentage is the percentage by which you will allow the Total Disk Space limit to be exceeded. I'm going to set mine at 0%.
15. The **Daemon Port** should be changed from `8080` to `443`, since we're going to run the node from behind a reverse proxied URL, that uses SSL. And for basically all SSL things, it uses 443 as the default port. It's very important to make this change.
16. The **Daemon SFTP Port** should remain at its default value of `2022`. This is the port that every SFTP server created by Pterodactyl Wings will use.
17. Now you select **Create Node**: <img src="https://i.imgur.com/WfdMcBv.png" alt="" data-size="line">
18. After that, it'll continue to [IP and Port allocation](03d-ip-and-port-allocation.md) - so you can go ahead to the next step in this tutorial :thumbsup:

### GIF Guide

<figure><img src="https://i.imgur.com/c6ZEodn.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

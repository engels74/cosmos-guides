# 02) My Panel login page is blank

### My Panel login page is blank! Help! :sob:

If your Panel does not appear after you [create the URL for it](../../pterodactyl-setup/02-creating-urls/02a-create-url-for-pt-panel.md), there could be a number of reasons for this. You must ensure that you have carefully followed all of the steps up until the point where you create the URLs for the Panels.

After you've double-checked that you've completed [all of the steps](https://github.com/engels74/cosmos-test11/blob/main/troubleshooting/00-overview/broken-reference/README.md), you can try one of the following options. Try them one at a time; they don't require you to try them in any particular order, and the order doesn't matter.

### Option 1: Recreate the PHP/Laravel cache

1. If the database connected to the Panel behaves strangely, you can refresh its cache. This is fairly straightforward. If this works for you but you have to do it after each restart, something else is wrong with your setup. But for now, let's give it a shot!
2. Head to your favourite SSH terminal, and connect to your server.
3. Execute the following command:

```bash
docker exec -it pt-panel /bin/sh
```

4. This allows you to enter the docker container `pt-panel` and run bash commands from within it.
5. Execute this command:

```bash
php artisan optimize
```

6. This will clear the cache, and you should be able to access your Panel via the reverse proxy URL [you created](../../pterodactyl-setup/02-creating-urls/02a-create-url-for-pt-panel.md).
7. Exit the docker container by typing `exit` in the terminal.

[![asciicast](https://asciinema.org/a/B8A8QbMA33C9F9wxzAyePAfRy.svg)](https://asciinema.org/a/B8A8QbMA33C9F9wxzAyePAfRy)

### Option 2: Delete everything

This is more of a last resort. But if nothing works, or if you have to run `php artisan optimise` after every reboot, something probably went wrong during the installation of Pterodactyl. And you would sadly have to delete everything and try once more.

1. Turn off your `pt-panel`, `pt-database` and `pt-redis` container. You can do this through the Cosmos Server UI.
2. Head to your favourite SSH terminal, and connect to your server.
3. Execute the following command:

```bash
sudo rm -rf /srv/pterodactyl/*
```

{% hint style="danger" %}
**Be aware!** This will delete everything connected to the **Pterodactyl Panel**.\
This means all the settings and users will get deleted.\
You will still keep your Game Server files, as they are located elsewhere (`/var/lib/pterodactyl`).
{% endhint %}

4. Turn on your containers in the following order - and wait a few seconds between them so they have time to create the necessary files.
   1. `pt-redis`
   2. `pt-database`
   3. `pt-panel`
5. You should now be able to proceed with the guide from the "[Creating URLs](../../pterodactyl-setup/02-creating-urls/)" step.
6. If it still doesn't work, I'd suggest asking for assistance on the [Pterodactyl discord server](https://discord.gg/pterodactyl).

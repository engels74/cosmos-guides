# 02a) Create URL for pt-panel

### Creation of the `pt-panel` URL

1. Head into your Cosmos Server web UI, under ServApps.
2. Find the `pt-panel` container.
3. Under "**URLs**", select the `New (+)` button to create a new URL: <img src="https://i.imgur.com/ab43vnw.png" alt="" data-size="line">
4. Go down to the "**Use Host**" field, and change the `pt-panel.domain.com` to `pterodactyl.domain.com`. In my case, I'm changing mine from `pt-panel.engels.zip` to `pterodactyl.engels.zip`.

{% hint style="warning" %}
**Warning!** The URL you set here, must correspond to the one you set as `APP_URL` in the [Docker Compose example](../01-installing-pterodactyl/01a-the-docker-compose-example.md)
{% endhint %}

5. Select `Confirm` to create the URL.
6. You can press the `Refresh` button in Cosmos, if the URL doesn't show up immediately.

<figure><img src="https://i.imgur.com/4iSlT8y.gif" alt=""><figcaption></figcaption></figure>

6. You can head to the URL you created, and it **should** load the initial Pterodactyl login page.
7. If it doesn't, go to the [Troubleshooting section](https://github.com/engels74/cosmos-test11/blob/main/pterodactyl-setup/02-creating-urls/broken-reference/README.md) of this guide and see if there's anything there that can help.

<figure><img src="https://i.imgur.com/DCjGw9y.png" alt=""><figcaption></figcaption></figure>

### On to the next step!

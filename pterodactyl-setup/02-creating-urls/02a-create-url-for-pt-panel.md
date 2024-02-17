# 02a) Create URL for pt-panel

### Creation of the `pt-panel` URL

1. Head into your Cosmos Server web UI, under ServApps.
2. Find the `pt-stack` and select "**View Stack**"
3. Find the `pt-panel` container.
4. Under "**URLs**", select the `New (+)` button to create a new URL:

<figure><img src="https://i.imgur.com/4zDVDNK.png" alt="" width="375"><figcaption></figcaption></figure>

5. Go down to the "**Use Host**" field, and make sure it says the same, as you set it to in the `APP_URL` in the [Docker Compose example](../01-installing-pterodactyl/01a-the-docker-compose-example.md). In my case, it's `https://pt-panel.engels.zip`.

{% hint style="warning" %}
**Warning!** The URL you set here, must correspond to the one you set as `APP_URL` in the [Docker Compose example](../01-installing-pterodactyl/01a-the-docker-compose-example.md)
{% endhint %}

6. Select `Confirm` to create the URL.
7. You can press the `Refresh` button in Cosmos, if the URL doesn't show up immediately.

<figure><img src="https://i.imgur.com/s4BOImM.gif" alt=""><figcaption><p>Make sure your URL matches with the APP_URL, that you set in your Docker Compose example.</p></figcaption></figure>

8. You can head to the URL you created, and it **should** load the initial Pterodactyl login page.
9. If it doesn't, go to the [Troubleshooting section](broken-reference) of this guide and see if there's anything there that can help.

<figure><img src="https://i.imgur.com/xBbXWPQ.png" alt=""><figcaption><p>Yay! So far so good!</p></figcaption></figure>

### On to the next step!

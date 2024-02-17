# 02b) Create URL for pt-wings

### Creation of the `pt-wings` URL

1. Head into your Cosmos Server web UI, under ServApps.
2. Find the `pt-wings` container.
3. Under "**URLs**", select the `New (+)` button to create a new URL:

<figure><img src="https://i.imgur.com/evXFq14.png" alt="" width="375"><figcaption></figcaption></figure>

4. The container port should be changed from `80` to `443`. Otherwise, SSL/reverse proxying will not function.
5. Go down to the "**Use Host**" field, and make sure it says `pt-wings.domain.com` . In my case, it's going to be `pt-wings.engels.zip`.

{% hint style="info" %}
**NB:** You can basically choose whatever URL you want for `pt-wings`, you just need to remember it for later. I'm going to choose `pt-wings` for my subdomain, and use that for the rest of tutorial.
{% endhint %}

6. Select `Confirm` to create the URL.
7. You can press the `Refresh` button in Cosmos, if the URL doesn't show up immediately.

<figure><img src="https://i.imgur.com/1PJZt31.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

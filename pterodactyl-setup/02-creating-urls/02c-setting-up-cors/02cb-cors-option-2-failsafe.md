# 02cb) CORS Option 2 (failsafe)

### Setting up CORS (failsafe)

1. We must enable CORS so that the `pt-panel` can connect to the reverse-proxied `pt-wings` URL and vice versa.
2. To accomplish this, we must navigate to the `pt-wings` URL settings. In my case, I choose the `pterodactylnode.engels.zip` settings-wheel. <img src="https://i.imgur.com/ZnvotJJ.png" alt="" data-size="line">
3. In there, go to the "**Security**" tab.
4. Scroll down to the "**Custom CORS Origin"**
5. Write a single `*` in the **Custom CORS Origin** field, and press `Save`.

<figure><img src="https://i.imgur.com/70H51F5.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

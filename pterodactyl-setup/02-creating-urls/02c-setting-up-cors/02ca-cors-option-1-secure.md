# 02ca) CORS Option 1 (secure)

### Setting up CORS (secure)

1. We must enable CORS so that the `pt-panel` can connect to the reverse-proxied `pt-wings` URL and vice versa.
2. To accomplish this, we must navigate to the `pt-wings` URL settings. In my case, I choose the `pt-wings.engels.zip` settings-wheel. <img src="https://i.imgur.com/SWILIh4.png" alt="" data-size="line">
3. In there, go to the "**Security**" tab.
4. Scroll down to the "**Custom CORS Origin"**
5. Write the url of your `pt-panel` in the **Custom CORS Origin** field, and press `Save`.
6. In my case, that would be: `https://pt-panel.engels.zip`. Remember to include the `https://`.

<figure><img src="https://i.imgur.com/03QlI0I.gif" alt=""><figcaption><p>Safe and secure :)</p></figcaption></figure>

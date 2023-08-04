# 04c) Creating a DNS Zone API Key

### Creating the DNS Zone API Key

Back in the step named [Cosmos hostname setup](../03-cosmos-hostname-setup.md), we left off at this part, where we had to enter information about the "DNS Challenge".

We will continue where we left off!

1. We're going to need to create a DNS API Token, that we can put into the `CLOUDFLARE_DNS_API_TOKEN` in the Cosmos Setup.
2. To do that, we need to head to the [Cloudflare API Dashboard](https://dash.cloudflare.com/profile/api-tokens).
3. In there, select "**Create Token**"

<figure><img src="https://i.imgur.com/784KE2F.png" alt=""><figcaption></figcaption></figure>

4. In the next step, select to use the "**Edit zone DNS**" template

<figure><img src="https://i.imgur.com/N0yCxQg.png" alt=""><figcaption></figcaption></figure>

5. In the next step, find where it says "Zone Resources" and select your domain in the box where it's currently saying `Select...`

<figure><img src="https://i.imgur.com/g7Qg5JH.png" alt=""><figcaption></figcaption></figure>

6. Select the "**Continue to summary**" button at the bottom of the page: <img src="https://i.imgur.com/iK3ycvi.png" alt="" data-size="line">
7. In the next menu, select "**Create Token**":

<figure><img src="https://i.imgur.com/jFlBGAT.png" alt=""><figcaption></figcaption></figure>

8. Now you'll get the `CLOUDFLARE_DNS_API_TOKEN` token. Remember to copy it!

<figure><img src="https://i.imgur.com/7PlljDJ.png" alt=""><figcaption></figcaption></figure>

### On to the next step!

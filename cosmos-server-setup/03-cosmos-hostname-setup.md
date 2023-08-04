# 03) Cosmos hostname setup

### Cosmos hostname setup

You'll need to set up your hostname/domain. In my case, I'm using Cloudflare and a "proper" domain, so this guide will be written from that perspective. I apologize if your DNS service looks drastically different.

You may not need a literal domain; instead, enter your local IPv4 address.

I'm also going to configure my domain with a wildcard certificate because I don't want to create A and/or CNAME records for each subdomain - and because Cloudflare actually supports it quite well :innocent:

However, in this guide, I'll be using my newly purchased testdomain `www.engels.zip`.

{% hint style="warning" %}
**Remember** to keep the Cosmos Server setup tab open, until you're finished.\
**Open a new tab**, if you need to configure Cloudflare or other DNS providers.
{% endhint %}

### Hostname setup

1. You can enter either a domain that you own, or your local IP address as your domain. In my case, I'm going to use my domain `engels.zip`.
2. Select the Let's Encrypt option, if you got a web-domain. Otherwise, you should select "Generate self-signed certificate".

<figure><img src="https://i.imgur.com/ALCbU97.png" alt="" width="375"><figcaption></figcaption></figure>

3. After that, I'm going to select `Cloudflare` as my DNS provider.

<figure><img src="https://i.imgur.com/JaN04lJ.png" alt="" width="375"><figcaption></figcaption></figure>

4. For the next part, I'll need to do the "DNS Challenge setup". All this is not needed, if you don't have a web-domain. So you can skip the DNS Challenge part, if you just use your local IP.

{% hint style="warning" %}
**You should keep the Cosmos Setup tab open, while you configure Cloudflare and the parts needed for the DNS Challenge!**
{% endhint %}

### On to the next step!

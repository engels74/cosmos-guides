# 04b) SSL Wildcard setup

### SSL Wildcard setup

To ensure that SSL Wildcards work with Cosmos, we must configure the DNS settings correctly. When you know what to do, it's fairly easy.

SSL Wildcards are clever because they use the root domain's SSL certificate for all subdomains. As a result, you do not need to create separate A or CNAME records for each subdomain you wish to create. You simply create URLs with Cosmos, and it will automatically work with SSL encryption/HTTPS. I promise it's fantastic!

### Setup an "A" record

1. Head to DNS
2. Setup a **A** name record:
3. Select "**(+) Add Record**"
4. For Type, select "A"
5. For Name, type in your web domain. In my case, it's `engels.zip`.
6. For IPv4 address, type in your Public IPv4 of the server hosting Cosmos Server
7. Turn off Cloudflare's Proxy Tunnel. It messes up certain things unfortunately.
8. Press Save

<figure><img src="https://i.imgur.com/hE7XrIa.png" alt=""><figcaption></figcaption></figure>

### Setup a "CNAME" record

1. Head to DNS
2. Setup a **CNAME** record:
3. Select "**(+) Add Record**"
4. For Type, select "**CNAME**"
5. For Name, type in `*` and nothing else.
6. For "Target", type in your web-domain of the server hosting Cosmos Server
7. In my case, it would be `engels.zip`
8. Turn off Cloudflare's Proxy Tunnel. It messes up certain things unfortunately.
9. Press Save

<figure><img src="https://i.imgur.com/gKawY7R.png" alt=""><figcaption></figcaption></figure>

### GIF Guide

Here's the whole process in a GIF, should you prefer that:

<figure><img src="https://i.imgur.com/DoW6Goz.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

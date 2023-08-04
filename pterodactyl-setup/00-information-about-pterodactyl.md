# 00) Information about Pterodactyl

### What is Pterodactyl?

Pterodactyl® is a free, open-source game server management panel built with PHP, React, and Go. Designed with security in mind, Pterodactyl runs all game servers in isolated Docker containers while exposing a beautiful and intuitive UI to end users.

### What is the difference between Pterodactyl Panel and Wings?

Pterodactyl is divided into two sections: the Panel (frontend) and the Wings (backend).

The **Panel** is essentially just a web interface with some dependencies. It employs'mariadb' as its database and'redis' as its cache.

Pterodactyl's **Wings** are its backbone. Pterodactyl's server control plane is Wings, which creates servers and manages their individual SFTP servers. It's all very cool!

### Why is this guide necessary?

Because it's a huge _PITA_ to setup, if you don't know where to begin, and know the weird quirks of setting Pterodactyl up, using Docker.

Ideally, both the Panel and the Wings should be behind Reverse Proxy. In my experience, it works best this way. So that's what we'll be doing in this guide.

It requires _some_ effort, but once set up, it's a very useful tool. It should work if you follow this guide and the previous steps.

I'll also demonstrate how to import different game servers, known as "eggs," and how to set up game servers in general using Pterodactyl. This will be covered in the [Using Pterodactyl](https://github.com/engels74/cosmos-test11/blob/main/pterodactyl-setup/broken-reference/README.md) section.

{% hint style="info" %}
**Disclaimer:**\
This guide was created with a fresh VPS and a fresh domain. I'm using Cloudflare as my DNS provider, with a Wildcard SSL certificate. I've tested the steps multiple times, formatting and starting over, and they should work across multiple systems.\\

Your mileage of success might vary. But it has worked for me and a few others, so hopefully it'll work for you to.

But **please** do not skip any of the steps, or something might break along the ride!
{% endhint %}

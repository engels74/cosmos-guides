# 03ba) Allocation Management

### Allocation Management

Okay, so I might need to explain this bit one more time.

Port allocation for **SteamCMD** servers, differs a bit from, say, a Minecraft server.

We previously discovered that **V Rising** required [three ports in total](../../02-importing-new-eggs/02a-locating-the-egg.md). There is one game port, one query port, and one RCON port.

This means we'll need one default allocated port and two additional ports.

In my case, I'm using `35001` (game), `35002` (query), and `35003` (RCON).

<figure><img src="https://i.imgur.com/JAYUeOy.gif" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/LfNxHOH.png" alt=""><figcaption><p>I hope it makes sense</p></figcaption></figure>

We need to remember these ports for when we get to the actual Services Variables setup.

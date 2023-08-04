# 02a) Locating the egg

### Locating the egg

For this tutorial, I'm going to import an egg for Valheim with BepInEx enabled.

1. Go to the [Egg repository](https://github.com/parkervcp/eggs#game-eggs), locate and then select **V Rising Vanilla**.

![](https://i.imgur.com/En1BU8G.png)

2. In there, you'll see the entire [README](https://github.com/parkervcp/eggs/tree/master/game\_eggs/steamcmd\_servers/v\_rising/v\_rising\_vanilla) for that egg

![](https://i.imgur.com/Yf9PyWt.png)

3. Most importantly, what you want to take note of are the **Server Ports**.
4. It is typically divided into "**Game**" and "**Query**" ports. When you create a new server, you allocate the "Game" port in the "**Default Allocation**" field. However, when configuring the server, you will usually have to manually change the Query port. If that sounds confusing right now, I'll explain when we're ready to create the server.

<figure><img src="https://i.imgur.com/qhDIVnj.png" alt=""><figcaption></figcaption></figure>

4. The default V Rising ports in this case are `9876` for the Game port and `9877` for the Query port. And then `25575` for the RCON port. But these ports can be changed into whatever you'd like.

![](https://i.imgur.com/WCQSwW6.png)

5. The important thing here is to **count** how many ports the game server requires and remember that number for when we build the server. Because the "**V Rising**" server requires three ports (game, query, and RCON), we require **three ports** in total.

![](https://i.imgur.com/oKsWgnJ.png)

6. This includes the one for Default Allocation. In total, we need the default allocated port, plus two additional allocated ports for the query and RCON ports.

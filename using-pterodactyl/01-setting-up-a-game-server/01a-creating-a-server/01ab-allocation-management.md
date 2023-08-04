# 01ab) Allocation Management

#### Allocation Management

1. The **Node** it defaults to is the one we just configured in the previous steps. So we can leave it at that.
2. For **Default Allocation**, it selects the port with the lowest number of available ports. If your friends want to connect to your server, the port it selects is usually the one you need to send them. In my case, the port the Minecraft server will use is `35001`.
3. You can allocate more ports to the game server under **Additional Allocation(s)**.\
   For Minecraft, this could be useful if you need, say, the BluMap addon and want to give other friends access to the BluMap Web UI.\
   Then you'd need to designate another port for that, in my case `35002`. Then, in my BluMap configuration, I'd enter that port, which is now connected to the Minecraft game server.

{% hint style="info" %}
**Some eggs** require more than one port, so remember to read the egg descriptions.\
Most Steam-based servers use atleast two ports; the base game port + the Steam Query port.
{% endhint %}

<figure><img src="https://i.imgur.com/aw7QNU7.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

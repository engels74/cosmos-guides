# 01ba) Startup Configuration

### Startup Configuration

We can modify the server launch command parameters in the Startup Configuration. For Minecraft, the server is allocated 128MB of RAM by default. That seems a little low to me, so I'll change the startup command to allow for a little more RAM, say 1GB.

You can do this by changing the `-Xms128M` to `-Xms1G`, making the entire startup command look like this:

```bash
java -Xms1G -XX:MaxRAMPercentage=95.0 -Dterminal.jline=false -Dterminal.ansi=true -jar {{SERVER_JARFILE}}
```

<figure><img src="https://i.imgur.com/wBkgjpW.gif" alt=""><figcaption></figcaption></figure>

### On to the next step!

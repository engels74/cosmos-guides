# 03c) Service Variables

### Startup Configuration

In this case, we must leave the Startup Command alone and not modify it. Unless explicitly stated in the README on Github, most custom eggs do not require us to change anything in the Startup Command.

### Service Variables (for V Rising)

I'm going to go over all of these options. V Rising have a lot of options!

They may differ from egg to egg, because some variables are game-specific, but the port variable settings are usually consistent across eggs.

`[REQUIRED] Server Query Port` = This is where we will configure the Query port. That would be the `35002` port that I [assigned to it](03b-game-server-configuration/03ba-allocation-management.md) in my case.

`Automatic Updates` = It can be either `0` or `1`. If you want to enable automatic updates, leave it at `1`, and if you want to disable them, change it to `0`. When you restart your server, the updates will take effect.

`Game Settings Preset` = Is a **V Rising** game-specific setting. It should already be described in the variable's description. It controls whether you want PvE or PvP, or other custom game modes.

`Server Name` = This is where you enter the name you want for your server. This is what other players will see when they use the server browser in the game.

`Server Description` = This is the description that players will see when they use the server browser in the game and want to learn more about your server.

`Max Connected Users` = Ought to be self-explanatory. How many people that can be on your server at the same time.

`Max Connected Admins` = Ought to be self-explanatory. How many admins can be on your server at the same time.

`Server Password` = Here you can configure the password required to access your server.

`Save Name` = Name of your save file for your world savefile.

`Auto Save Count` = How many autosaves (backups, essentially) do you want to keep at once.

`Auto Save Interval` = Interval in seconds between each autosave.

`List On Steam` = Ought to be self-explanatory. Can either be `true` or `false`.

`List On Epic` = Ought to be self-explanatory. Can either be `true` or `false`.

`[Repair] Validate Server Files` = Can either be `true` or left empty. If you set this to true, it'll validate all server files, every time you either start or restart the server.

`[Advanced] Server FPS` = Controls how often the server refreshes.

`[Advanced] Compress Save Files` = Set to `true` to compress world save files, else set to `false`.

`[Advanced] Enable API` = Set to `true` to allow responses to public API requests to the server, else set to `false`.

`[Advanced] Enable RCON` = Can either be `true` or `false`, whether or not you want to use RCON or not.

`[Advanced] RCON Port` = This is where we will configure the RCON port. That would be the `35003` port that I [assigned to it](03b-game-server-configuration/03ba-allocation-management.md) in my case.

`[Advanced] Secure Server` = Can either be `true` or `false`, whether or not you want to use encrypted packages or not (SSL or no SSL I guess)

`[Advanced] Admin Only Debug Events` = Only admin can debug events. Can either be `true` or `false`.

`[Advanced] Disable Debug Events` = Disable or enable debug events. Can either be `true` or `false`.

`[Advanced] V Rising Dedicated Server App ID` = This App ID refers to the ID from e.g. [SteamDB](https://steamdb.info/app/1829350/info/), for the dedicated server tool. **Do not change this!**

`[Advanced] Use Windows Branch` = We need this set to `1`, since there's no Linux version of the server yet.

`[SYSTEM] WINEDEBUG` = Just leave this setting on the default value. Wine specific setting.

`[SYSTEM] WINEARCH` = Just leave this setting on the default value. Wine specific setting.

`[SYSTEM] WINEPATH` = Just leave this setting on the default value. Wine specific setting.

### On to the next step!

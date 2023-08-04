# 03) QoL Docker Compose setup

### Creating some quick "shortcuts"

In this section, we'll add some quick "shortcuts" known as bash aliases in Linux. Working with Docker Compose containers will make your life easier.

1. Edit or create some new bash\_aliases with this command:

```bash
nano $HOME/.bash_aliases
```

2. Paste this in: (credits goes to [LSIO](https://docs.linuxserver.io/general/docker-compose#tips-and-tricks))

```bash
alias dcup='docker compose -f /opt/docker-all/docker-compose.yml up -d' #brings up all containers if one is not defined after dcup
alias dcdown='docker compose -f /opt/docker-all/docker-compose.yml stop' #brings down all containers if one is not defined after dcdown
alias dcpull='docker compose -f /opt/docker-all/docker-compose.yml pull' #pulls all new images unless one is specified
alias dclogs='docker compose -f /opt/docker-all/docker-compose.yml logs -tf --tail="50" '
alias dtail='docker logs -tf --tail="50" "$@"'
```

3. Now you can do the following, after you **exit** and then **reenter** your terminal:

```
dcup   = launches all the docker containers inside /opt/docker-all/docker-compose.yml
dcdown = stops all the docker containers inside /opt/docker-all/docker-compose.yml
dcpull = pulls new images for all the docker containers inside /opt/docker-all/docker-compose.yml
dclogs = will post the 50 newest lines from the logs of all docker containers the docker containers inside /opt/docker-all/docker-compose.yml
dtail  = you can now enter "dtail NameOfDockerContainer" and it'll give you the 50 newest lines from that particular container
```

4. The whole process should look something like this:

[![asciicast](https://asciinema.org/a/NXBtd74C9V3G92U7mVp7qWV9S.svg)](https://asciinema.org/a/NXBtd74C9V3G92U7mVp7qWV9S)

### On to the next step!

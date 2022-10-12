# Docker Minecraft Server

Shoutout to [itzg](https://github.com/itzg) of whom this project is forked.
For README.md of original project see [here](https://github.com/itzg/docker-minecraft-server#readme).

## Setting up project locally

1. Copy _[.env.template](.env.template)_ to _.env_ and complete unset variables as needed (Description can be found in [original project](https://github.com/itzg/docker-minecraft-server#readme))
2. Copy _[docker-compose.template.yml](docker-compose.template.yml)_ to _docker-compose.yml_
3. Build and run container by running `docker compose up`

## Setting world data

Use your custom world data by adding it to the data folder as follows.

1. Create data and world folder `mkdir -p data/world`
2. Add your world data to the folder
3. Uncomment the data volume mapping in the _docker-compose.yml_ file

## Setting player whitelist and op list if needed

1. Create players folder `mkdir -p players`
2. Add corresponding files to folder `touch players/whitelist.json | touch players/ops.json`
3. Add players data to the files as described [here](https://minecraft.fandom.com/wiki/Whitelist.json)
4. Uncomment the players volume mapping in the _docker-compose.yml_ file


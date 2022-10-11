# Shairport Sync
https://hub.docker.com/r/mikebrady/shairport-sync

Shairport Sync is an Apple AirPlay audio player.

```
mkdir -p $HOME/docker/shairport-sync/etc
```
```
cd $HOME/docker/shairport-sync
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/shairport-sync/docker-compose.yml
```
```
docker-compose pull
```
```
docker-compose up -d
```
Create a local copy of shairport-sync.conf if you need to make changes to the behavior of shairport-sync.
```
docker cp shairport-sync:/etc/shairport-sync.conf $HOME/docker/shairport-sync/etc/
```
Edit $HOME/docker/shairport-sync/shairport-sync.conf to your liking.

```
nano $HOME/docker/shairport-sync/etc/shairport-sync.conf
```
CTRL-X to save.

Edit docker-compose and make the following changes:
```
#     volumes:
#       - ./config/shairport-sync.conf:/etc/shairport-sync.conf # Customised Shairport Sync configuration file.
```
Change to:
```
     volumes:
       - ./config/shairport-sync.conf:/etc/shairport-sync.conf # Customised Shairport Sync configuration file.
```
Recreate and restart the container.
```
docker-compose up -d
```



## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)

# Shairport Sync
https://hub.docker.com/r/mikebrady/shairport-sync

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
```
docker cp shairport-sync:/etc/shairport-sync.conf $HOME/docker/shairport-sync/etc/
```
Now you have a local copy of shairport-sync.conf for editing as needed




Edit $HOME/docker/shairport-sync/shairport-sync.conf to your liking.

If you're using a device other than the Pi stereo jack,
uncoment the "volumes" section and the alsa.conf line
and edit alsa.conf appropriately to use either a USB soundcard
or DAC

If you need to make changes to shairport-sync.conf.
uncomment the Volumes and shairport-sync.conf lines in 
docker-compose.yml
```
nano $HOME/docker/shairport-sync/etc/shairport-sync.conf
```
```
docker container restart shairport-sync
```



## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)

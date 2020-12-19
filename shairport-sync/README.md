https://hub.docker.com/r/mikebrady/shairport-sync

If you're using a device other than the Pi stereo jack,
uncoment the "volumes" section and the alsa.conf line
and edit alsa.conf appropriately to use either a USB soundcard
or DAC

If you need to make changes to shairport-sync.conf.
uncomment the Volumes and shairport-sync.conf lines in 
docker-compose.yml
Copy shairport-sync from the docker container to local system.
```
mkdir $HOME/docker/shairport-sync/etc
```
```
docker cp shairport-sync:/etc/shairport-sync.conf $HOME/docker/shairport-sync/etc/
```
```
cd $HOME/docker/shairport-sync
```
```
docker-compose up -d
```

Edit $HOME/docker/shairport-sync/shairport-sync.conf to your liking.
```
nano $HOME/docker/shairport-sync/etc/shairport-sync.conf
```
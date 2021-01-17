# Unbound & Pihole
https://hub.docker.com/r/klutchell/unbound

Instructions for installing Pihole and klutchell's Unbound Docker image as stack with own netork.
```
mkdir $HOME/docker/unbound-pihole
```
```
cd $HOME/docker/unbound-pihole
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/unbound-pihole/docker-compose.yml
```
```
docker-compose pull
```
```
docker-compose up -d
```
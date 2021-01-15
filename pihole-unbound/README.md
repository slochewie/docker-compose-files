# Pi-Hole + Unbound
https://hub.docker.com/r/cbcrowe/pihole-unbound

https://github.com/chriscrowe/docker-pihole-unbound

```
mkdir -p $HOME/docker/pihole-unbound
```
```
cd $HOME/docker/pihole-unbound
```
```
wget https://github.com/chriscrowe/docker-pihole-unbound/raw/master/one-container/docker-compose.yaml
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/pihole-unbound/.env
```
Edit the .env file with your preferred variables.
```
nano .env
```
Make your changes and Ctrl-X and Y to save and exit
```
docker-compose pull
```
```
docker-compose up -d
```
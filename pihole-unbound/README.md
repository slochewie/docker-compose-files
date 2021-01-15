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
Edit the docker compose file with your preferred variables.
```
nano docker-compose.yml
```
Make your chnages and Ctrl-X and Y to save and exit
```
docker-compose pull
```
```
docker-compose up -d
```
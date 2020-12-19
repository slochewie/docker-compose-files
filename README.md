# docker-compose-files
These are the docker-compose.yml files I use most frequently use.
Most can be run as is with a simple "docker-compose up -d".
Some will require minor edits for pathing, etc.

None will work without Docker or Docker Compose installed.
Without further ado:

Install Docker & Docker Compose
```
sudo apt-get update
```
```
sudo apt-get upgrade
```
```
sudo apt-get install apt-transport-https ca-certificates software-properties-common
```
```
curl -fsSL get.docker.com -o get-docker.sh && sh get-docker.sh
```
Optional. Add user pi to the docker group. Run docker and docker-compose without sudo.
```
sudo usermod -aG docker pi
```
```
sudo apt-get install docker-compose
```

Now get the docker-compose.yml files

```
git clone https://github.com/slochewie/docker-compose-files.git
```
This will make a directory called docker-compose-files 
in $HOME/.
I'm not a fan of the directory name.
```
mv $HOME/docker-compose-files $HOME/docker
```

To install a container, cd into the directory of the container you
want to create and run "docker-compose up -d"
For example:
```
cd $HOME/docker/pihole
```
```
docker-compose up -d
```

To upgrade an existing container.
cd into the directory of the container you wish to upgrade.
For example:
```
cd $HOME/docker/pihole
```
```
docker-compose pull
```
```
docker-compose up -d
```
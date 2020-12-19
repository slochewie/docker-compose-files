# docker-compose-files
These are the docker-compose.yml files I use most frequently use.
Most can be run as is with a simple "docker-compose up -d".
Some will require minor exits for pathing, etc.

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
```
sudo usermod -aG docker pi
```
```
sudo apt-get install docker-compose
```
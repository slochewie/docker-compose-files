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


DEBIAN BASED DISTROS

The systemd-resolved service by default has DNSStubListener
listening on port 53. This will give an error when starting
the Docker container that uses port 53 as well.

```
sudo mkdir /etc/systemd/resolved.conf.d
```
```
sudo nano /etc/systemd/resolved.conf.d/adguardhome.conf
```
Paste in the following text (Ctrl+Shift+V)
```
[Resolve]
DNS=127.0.0.1
DNSStubListener=no
```
Ctrl+X to save and Y for yes
```
sudo mv /etc/resolv.conf /etc/resolv.conf.backup
```
```
ln -s /run/systemd/resolve/resolv.conf /etc/resolv.conf
```
Stop DNSStubListener while restarting systemd-resolved:
```
systemctl reload-or-restart systemd-resolved
```

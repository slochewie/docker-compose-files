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


DEBIAN BASED DISTROS

The systemd-resolved service by default has DNSStubListener
listening on port 53. This will give an error when starting
the Docker container that uses port 53 as well.

```
sudo mkdir /etc/systemd/resolved.conf.d
```
```
sudo nano /etc/systemd/resolved.conf.d/pihole.conf
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
sudo ln -s /run/systemd/resolve/resolv.conf /etc/resolv.conf
```
Stop DNSStubListener while restarting systemd-resolved:
```
sudo systemctl reload-or-restart systemd-resolved
```

If you stop the container your Pi will no longer be able to resolve dns.
So to undo the DEBIAN BASED DISTRO steps:
```
sudo rm /etc/resolv.conf
```
```
sudo mv /etc/resolv.conf.backup /etc/resolv.conf
```
```
sudo mv /etc/systemd/resolved.conf.d/pihole.conf /etc/systemd/resolved.conf.d/pihole.conf.backup
```
```
sudo systemctl reload-or-restart systemd-resolved
```

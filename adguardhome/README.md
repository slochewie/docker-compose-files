https://hub.docker.com/r/adguard/adguardhome

The systemd-resolved service by default ahs DNSStubListener 
listening on port 53. This will give an error when starting 
the Docker container that uses port 53 as well. The 
following instructions are the workaround given by adguardhome in
Step 8 of the above URL.

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
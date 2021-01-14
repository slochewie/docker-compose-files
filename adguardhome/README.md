https://hub.docker.com/r/adguard/adguardhome


```
sudo mkdir /etc/systemd/resolved.conf.d
```
```
/etc/systemd/resolved.conf.d/adguardhome.conf
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
``
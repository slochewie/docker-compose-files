# Portainer
https://hub.docker.com/r/portainer/portainer-ce

This Docker compose file will create Portainer. Uncommenting sections will allow for Portainer Agent and Let's Encrypt SSL certs created by certbot.

```
mkdir -p /home/pi/docker/portainer-ce
```
```
cd /home/pi/docker/portainer-ce
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/portainer/docker-compose.yml
```
```
docker-compose pull
```
```
docker-compose up -d
```



## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)
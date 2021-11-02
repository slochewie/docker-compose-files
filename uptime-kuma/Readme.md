# Uptime Kuma
https://hub.docker.com/r/derkades/raspotify

Installs uptime kuma

```
mkdir -p $HOME/docker/uptime-kuma
```
```
cd $HOME/docker/uptime-kuma
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/raspotify/docker-compose.yml
```
```
docker-compose pull
```
```
docker-compose up -d
```

Browse to http://ip-address:3001

## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)
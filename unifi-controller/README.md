# Unifi Controller
https://hub.docker.com/r/linuxserver/unifi-controller

Edit the docker-compose.yml as needed for your installation such as ports. If you require access from outside your local network poke holes in your router's firewall as needed.

```
mkdir -p $HOME/docker/unifi-controller
```
```
cd $HOME/docker/unifi-controller
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
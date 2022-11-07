# Heimdall
- https://heimdall.site/
- https://docs.linuxserver.io/images/docker-heimdall
- https://hub.docker.com/r/linuxserver/heimdall
Heimdall Application Dashboard is a dashboard for all your web applications. It doesn't need to be limited to applications though, you can add links to anything you like. There are no iframes here, no apps within apps, no abstraction of APIs. if you think something should work a certain way, it probably does
```
mkdir -p $HOME/docker/heimdall
```
```
cd &HOME/docker/heimdall
```
```
wget https://raw.githubusercontent.com/slochewie/docker-compose-files/main/heimdall/docker-compose.yml
```
docker-compose pull
```
```
docker-compose up -d
```
Go to:
http://your-pi-ip

## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)

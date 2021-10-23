# Homer
https://hub.docker.com/r/b4bz/homer

```
mkdir -p /home/pi/docker/homer
```
```
cd /home/pi/docker/homer
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/homer/docker-compose.yml
```
Edit config.yml to your liking.
```
nano ./assets/config.yml
```
Ctrl+O to save. Ctrl+X to exit.
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

[MIT License](./L
# Pihole
https://hub.docker.com/r/pihole/pihole

Standard Docker Compose instructions.
Make a directory for the docker-compose.yml file.
For example:
```
mkdir -p /home/pi/docker/pihole
```
```
cd /home/pi/docker/pihole
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/pihole/docker-compose.yml
```
```
docker-compose pull
```
```
docker-compose up -d
```

Verify its working by going to
http://ip-of-your-pi


## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)
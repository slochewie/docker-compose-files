# Home Assistant, Mosquitto, and Zigbee2MQTT
- https://www.home-assistant.io
- https://hub.docker.com/r/homeassistant/home-assistant
- https://hub.docker.com/_/eclipse-mosquitto
- https://github.com/Koenkk/zigbee2mqtt

```
mkdir -p $HOME/docker/hass
```
```
cd &HOME/docker/hass
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/hass/docker-compose.yml
```
```
docker-compose pull
```
```
docker-compose up -d
```

Go to:

Home-Assistant
http://your-pi-ip:8123

Zigbee2MQTT
http://your-pi-ip:8989

## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)

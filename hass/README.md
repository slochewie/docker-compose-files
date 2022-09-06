# Home Assistant, Mosquitto, and Zigbee2MQTT
- https://www.home-assistant.io
- https://hub.docker.com/r/homeassistant/home-assistant
- https://hub.docker.com/_/eclipse-mosquitto
- https://github.com/Koenkk/zigbee2mqtt

## Installation
```
mkdir -p $HOME/docker/hass
```
```
cd $HOME/docker/hass
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
Edit configuration.yml to your needs
```
nano configuration.yml
```
```
sudo mv configuration.yml ./zigbee2mqtt/data/
```

Edit mosquito.conf to your needs
```
nano mosquitto.conf
```
```
sudo mv mosquito.conf ./mosquitto/config/
```
The Mosquitto container runs the mosquitto server under UID 1883 and GID 1883. To avoid read/write errors, chown the mosquitto directory as 1883:1883
```
sudo chown -R 1883:1883 ./mosquitto
```

Restart Mosquitto and Zigbee2MQTT
```
docker-compose restart mosquitto zigbee2mqtt
```


## To update all
```
docker-compose pull
```
```
docker-compose up -d
```

## To update Home Asssitant
```
docker-compose pull homeassistant
```
```
docker-compose up -d homeassistant
```

## To update Mosquitto
```
docker-compose pull mosquitto
```
```
docker-compose up -d mosquitto
```

## To update Zigbee2MQTT
```
docker-compose pull zigbee2mqtt
```
```
docker-compose up -d zigbee2mqtt
```

## To restart Home Assistant
```
docker-compose restart homeassistant
```

## To restart Mosquitto
```
docker-compose restart mosquitto
```

## To restart Zigbee2MQTT
```
docker-compose restart zigbee2mqtt
```

## Home Assistant and Zigbee2MQTT web admins

Home Assistant
http://server-ip:8989

Zigbee2MQTT
http://server-ip:8989

## Author

Aaron Wilson <https://niteowl.dev>

[![](https://cdn.buymeacoffee.com/buttons/default-blue.png)](https://www.buymeacoffee.com/slochewie)

## License

[MIT License](./LICENSE)
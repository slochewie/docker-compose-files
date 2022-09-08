# Home Assistant, Mosquitto, and Zigbee2MQTT
- https://www.home-assistant.io
- https://hub.docker.com/r/homeassistant/home-assistant
- https://mosquitto.org/
- https://hub.docker.com/_/eclipse-mosquitto
- https://www.zigbee2mqtt.io/
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
Edit Zigbee2MQTT's configuration.yml to your needs
```
nano configuration.yml
```
```
sudo mv configuration.yml ./zigbee2mqtt/data/
```

Edit Mosquitto's mosquito.conf to your needs. By default the existing file should work as is with no authentication needed. This is fine for initial usage making sure it works, but authentication should be added.
```
nano mosquitto.conf
```
```
sudo mv mosquito.conf ./mosquitto/config/
```
The Mosquitto container runs the mosquitto server under UID 1883 and GID 1883. I've tried changing this in the docker-compose file with no luck. My workaround to avoid read/write errors is to chown the mosquitto directory with 1883:1883
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

## Adding Mosquitto User Authentication
Out of the box, the included mosquitto.conf file, user authentication will be disabled and allow anonymous connections. Perform the following steps to setup user authentication and disable anonymous connections to Mosquitto.

Change <user> to an user of your liking. This user and password will also be used in Home Assistant when adding MQTT support. I use hass_mqtt as the user but it's totally up to you.
```
docker-compose exec mosquitto mosquitto_passwd -c /mosquitto/config/password_file <user>
```
You'll be prompted for a password twice. Enter it twice.


Now edit the mosquitto conf file.
```
nano ,/mosquitto/config/mosquitto.config
```
Find the line
```
allow_anonymous true
```
Change it to
```
allow_anonymous false
```
Find the line
```
#password_file
```
Change it to
```
password_file /mosquitto/config/password_file
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

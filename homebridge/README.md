# Homebridge
https://hub.docker.com/r/oznu/homebridge

https://github.com/oznu/docker-homebridge

This will get Homebridge with the Web GUI up and running in no time using Docker. I used Homebridge for years but have recently switched all my Raspberry Pis to Home Assistant. I wanted to create my own ZigBee hub to replace a Philips Hue hub. Home Assistant with Mosquitto and Zigbee2MQTT seems to be the way. For instructions on how to do that see: https://github.com/slochewie/docker-compose-files/tree/main/hass 

```
mkdir -p /home/pi/docker/homebridge
```
```
cd /home/pi/docker/homebridge
```
```
wget https://github.com/slochewie/docker-compose-files/raw/main/homebridge/docker-compose.yml
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

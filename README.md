# docker-compose configuration for mosquitto and mqtt-explorer

## Initialization

`docker-compose up -d`

## Mqtt-Explorer

`Go to localhost:4000 for client` 

```
Protocol: mqtt://

Host: mqtt

Port: 1883
```
Websocket protocol is enabled.
```
Protocol: ws://

Host: mqtt

Port: 8080
```

## Authentication

Authentication is disabled by default.

To enable it, edit mosquitto/conf/mosquitto.conf file. After enable authentication default username and password is admin/admin

## To Create New User

To create new user run command below while mqtt is running:

`docker-compose exec mosquitto mosquitto_passwd -b /mosquitto/config/mosquitto.passwd admin 123456`

## Send test message to mqtt
       
Run command below

`docker run -it --rm --net=host efrecon/mqtt-client pub -h localhost -p 1883 -t "test/device" -m "test message"`

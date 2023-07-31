# docker-compose configuration for mosquitto

## Initialization

`docker-compose up -d`

## To Create New User

`docker-compose exec mosquitto mosquitto_passwd -b /mosquitto/conf/mosquitto.passwd admin 123456`

Default username and password is admin/admin
       

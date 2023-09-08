# sm-server

InfluxDB + MQTT server using Docker containers. Use `sh/env_setup` to populate environment variables, then `docker compose up` to create the service. This will create a "telegraf" MQTT user for internal communication. After this, you can create or delete additional MQTT users using:
```sh
sh/mqtt_adduser <username>
sh/mqtt_adduser -b <username> <password>
sh/mqtt_deluser <username>
```
These users are stored in the password file `./etc/mosquitto/passwd`.

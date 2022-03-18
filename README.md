# ble2mqtt-docker

Image docker pour le projet [ble2mqtt](https://github.com/devbis/ble2mqtt)

---

### Docker compose

```
version: "3"
services:
  ble2mqtt:
    container_name: ble2mqtt
    image: ble2mqtt:latest
    networks:
      - host
    privileged: true
    restart: always
    volumes:
      - /data/ble2mqtt:/data
      - /var/run/dbus:/var/run/dbus
```

#### Volume

dossier ou ce trouve le fichier [json](https://github.com/devbis/ble2mqtt#configuration)

> /path/to/data:/data

---

### Docker commande

```
docker run \
-d \
--net=host \
-v /data/ble2mqtt:/data \
-v /var/run/dbus:/var/run/dbus \
ble2mqtt:latest
```

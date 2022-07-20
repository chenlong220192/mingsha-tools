- zabbix-server
```
docker run \
    -d \
    --name zabbix-java-gateway \
    --network=zabbix-net \
    zabbix/zabbix-java-gateway:alpine-5.2-latest
```

- docker run
```
docker run \
    -d \
    -p 9099:8080 \
    --env admin.registry.address=zookeeper://192.168.1.1:2181 \
    --env admin.config-center=zookeeper://192.168.1.1:2181 \
    --env admin.metadata-report.address=zookeeper://192.168.1.1:2181 \
    --name=dubbo-admin \
    apache/dubbo-admin
```

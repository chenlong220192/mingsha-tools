- docker run
```
docker run \
    -d \
    -p 7000:7000 \
    -v /data/containers/redis-6.2.7/master-slave/master:/data \
    --entrypoint redis-server /data/redis.conf \
    --memory 16m \
    --name redis-master \
    redis:6.2.7-alpine3.16
```
```
docker run \
    -d \
    -p 7001:7001 \
    -v /data/containers/redis-6.2.7/master-slave/slave:/data \
    --entrypoint redis-server /data/redis.conf \
    --memory 16m \
    --name redis-slave \
    redis:6.2.7-alpine3.16
```

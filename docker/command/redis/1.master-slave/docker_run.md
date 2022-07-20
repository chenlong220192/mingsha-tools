- docker run
```
docker run \
    -d \
    -p 7000:7000 \
    -v /data/container/redis/6.2.1/master-slave/master:/data \
    --entrypoint redis-server /data/redis.conf \
    --memory 16m \
    --name redis-master \
    redis:6.2.7-alpine
```
```
docker run \
    -d \
    -p 7001:7001 \
    -v /data/container/redis/6.2.1/master-slave/slave:/data \
    --entrypoint redis-server /data/redis.conf \
    --memory 16m \
    --name redis-slave \
    redis:6.2.7-alpine
```

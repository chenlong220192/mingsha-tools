- redis
```
docker run \
    -d \
    -p 0.0.0.0:6379:6379 \
    -v /volume1/docker/redis:/data \
    --memory 128m \
    --restart=no \
    --name redis \
    redis:6.2.7-alpine3.16
```

- docker run
```
docker run \
    -d \
    -p 0.0.0.0:6379:6379 \
    -v /data/containers/redis:/data \
    --memory 128m \
    --name redis \
    redis:7.2.4-alpine
```

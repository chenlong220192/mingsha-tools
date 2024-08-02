- docker run
```
docker run -d \
    -p 5555:5000 \
    -v /data/containers/registry:/var/lib/registry \
    --name registry \
    registry:2.8.3
```

- docker run
```
docker run \
    -d \
    --name alist \
    --restart=no \
    --memory 256m \
    -v /volume1/docker/alist:/opt/alist/data \
    -p 5244:5244 \
    -e PUID=0 \
    -e PGID=0 \
    -e UMASK=022 \
    xhofe/alist:latest
```

- docker run
```
docker run -d \
      -p 8000:8000 \
      -p 9000:9000 \
      -v /var/run/docker.sock:/var/run/docker.sock \
      -v /data/container/portainer:/data \
      --name portainer \
      portainer/portainer:alpine
```

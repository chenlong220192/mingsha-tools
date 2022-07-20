- docker run
```
docker run -d \
      -p 9000:9000 \
      -v /var/run/docker.sock:/var/run/docker.sock \
      -v /volume1/docker/portainer:/data \
      --name portainer \
      --restart=always \
      --memory 256m \
      portainer/portainer:alpine
```

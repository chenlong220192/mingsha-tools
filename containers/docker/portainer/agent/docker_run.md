- docker run
```
docker run \
      -d \
      -it \
      --restart=always \
      -p 9001:9001 \
      -v /var/run/docker.sock:/var/run/docker.sock \
      -v /var/lib/docker/volumes:/var/lib/docker/volumes \
      --name portainer_agent \
      portainer/agent
```

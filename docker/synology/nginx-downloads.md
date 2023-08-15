- nginx-downloads
```
  docker run \
      -d \
      -p 9011:80 \
      -v /volume1/docker/nginx-downloads/resources:/app \
      -v /volume1/docker/nginx-downloads/conf.d:/etc/nginx/conf.d \
      --restart always \
      --memory 128m \
      --name nginx-downloads \
      nginx:1.23.1-alpine
```

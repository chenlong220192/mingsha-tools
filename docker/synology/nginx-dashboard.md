- nginx-dashboard
```
  docker run \
      -d \
      -p 8080:80 \
      -v /volume1/docker/nginx-dashboard/dashboard:/app \
      -v /volume1/docker/nginx-dashboard/conf.d:/etc/nginx/conf.d \
      --restart always \
      --memory 128m \
      --name nginx-dashboard \
      nginx:1.23.1-alpine
```

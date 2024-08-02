- docker run
```
docker run -d \
      -p 8085:8080 \
      --name adminer \
      --restart=always \
      --memory 256m \
      adminer:latest
```

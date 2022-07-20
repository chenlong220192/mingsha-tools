- mysql 5.7
```
docker run \
    -d \
    -p 3306:3306 \
    -e MYSQL_ROOT_PASSWORD=123456 \
    --name mysql \
    --restart=always \
    --memory 1024m \
    mysql:5.7.31
```

- mysql 5.7
```
docker run \
    -d \
    -p 0.0.0.0:3306:3306 \
    -e MYSQL_ROOT_PASSWORD=123456 \
    -v /volume1/docker/mysql/etc/mysql/:/etc/mysql/ \
    -v /volume1/docker/mysql/var/lib/mysql/:/var/lib/mysql/ \
    --memory 1024m \
    --restart=no \
    --name mysql \
    mysql:5.7.31
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp mysql:/etc/mysql/ /volume1/docker/mysql/etc/`
  - `docker cp mysql:/var/lib/mysql/ /volume1/docker/mysql/var/lib/`

- mysql 5.7
```
docker run \
    -d \
    -p 3306:3306 \
    -e MYSQL_ROOT_PASSWORD=123456 \
    --name mysql \
    mysql:5.7.31
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp mysql_5.7:/etc/mysql/ /data/docker/mysql_5.7/etc/`
  - `docker cp mysql_5.7:/var/lib/mysql /data/docker/mysql_5.7/var/lib/`


- mysql 8.0
```
docker run \
    -d \
    -p 3306:3306 \
    -p 33060:33060 \
    --restart=always \
    --name mysql-8.0.24 \
    -e MYSQL_ROOT_PASSWORD="123456" \
    mysql:8.0.24 \
    --character-set-server=utf8 \
    --collation-server=utf8_bin \
    --default-authentication-plugin=mysql_native_password
```

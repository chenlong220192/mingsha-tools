- mysql 5.7
```
docker run \
    -d \
    -p 3306:3306 \
    -e MYSQL_ROOT_PASSWORD=123456 \
    -v /data/containers/mysql-5.7.31/etc/mysql/:/etc/mysql/ \
    -v /data/containers/mysql-5.7.31/var/lib/mysql/:/var/lib/mysql/ \
    --name mysql-5.7.31 \
    mysql:5.7.31
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp mysql-5.7.31:/etc/mysql/conf.d/ /data/containers/mysql-5.7.31/etc/mysql/`
  - `docker cp mysql-5.7.31:/var/lib/mysql/ /data/containers/mysql-5.7.31/var/lib/`


- mysql 8.0
```
docker run \
    -d \
    -p 3306:3306 \
    -v /data/containers/mysql-8.0.24/etc/mysql:/etc/mysql/ \
    -v /data/containers/mysql-8.0.24/var/lib/mysql:/var/lib/mysql/ \
    --restart=always \
    --name mysql-8.0.32 \
    -e MYSQL_ROOT_PASSWORD="123456" \
    mysql:8.0.32 \
    --character-set-server=utf8 \
    --collation-server=utf8_bin \
    --default-authentication-plugin=mysql_native_password
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp mysql-8.0.24:/etc/mysql/conf.d/ /data/containers/mysql-8.0.24/etc/mysql/`
  - `docker cp mysql-8.0.24:/var/lib/mysql/ /data/containers/mysql-8.0.24/var/lib/`

- skywalking-oap-server
```
docker run \
-d \
-p 1234:1234 \
-p 11800:11800 \
-p 12800:12800 \
--name skywalking-oap-server \
apache/skywalking-oap-server:latest
```

- skywalking-ui
```
docker run \
-d \
-p 8080:8080 \
--name skywalking-ui \
-e TZ=Asia/Shanghai \
--link skywalking-oap-server:skywalking-oap-server \
apache/skywalking-ui:latest \
--collector.ribbon.listOfServers=skywalking-oap-server:12800 \
--security.user.admin.password=123456
```

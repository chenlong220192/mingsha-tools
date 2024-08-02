- docker run
```
docker run -d \
  -p 8200:8200 \
  -e "discovery.type=single-node" \
  -v /data/docker/ELK/apm-server:/usr/share/apm-server \
  --name apm-server \
  docker.elastic.co/apm/apm-server:7.7.0
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp apm-server:/usr/share/apm-server /data/docker/ELK/`

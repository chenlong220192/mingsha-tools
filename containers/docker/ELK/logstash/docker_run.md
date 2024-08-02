- docker run
```
docker run -d \
  -v /data/docker/ELK/logstash:/usr/share/logstash \
  --name logstash \
  docker.elastic.co/logstash/logstash:7.7.0
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp logstash:/usr/share/logstash /data/docker/ELK/`

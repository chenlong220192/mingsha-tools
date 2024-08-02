- docker run
```
docker run -d \
  -p 5601:5601 \
  -v /data/container/kibana:/usr/share/kibana \
  --name kibana \
  elastic/kibana:7.12.1
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp kibana:/usr/share/kibana /data/docker/ELK/`
- 修改`config/kibana.yml`配置elasticsearc连接方式
  - elasticsearch.hosts: [ "http://ip:port" ]
  - elasticsearch.username: elastic
  - elasticsearch.password: changeme

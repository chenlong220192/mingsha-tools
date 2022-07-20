- 单机版
```
docker run -d \
  -p 9200:9200 -p 9300:9300 \
  -e "discovery.type=single-node" \
  --name elasticsearch \
  elastic/elasticsearch:7.12.1
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp elasticsearch:/usr/share/elasticsearch /data/container/`

- CentOS7虚拟机配置
`vim /etc/sysctl.conf`
增加:
`vm.max_map_count = 262144`

- 权限
`chown -R 1000:1000 *``

- 集群版
```
docker run \
    -d \
    -p 9200:9200 \
    -p 9300:9300 \
    -v /data/container/elasticsearch/elasticsearch_node01:/usr/share/elasticsearch \
    --name elasticsearch_node01 \
    elastic/elasticsearch:7.12.1
```

```
docker run \
    -d \
    -p 9201:9201 \
    -p 9301:9301 \
    -v /data/container/elasticsearch/elasticsearch_node02:/usr/share/elasticsearch \
    --name elasticsearch_node02 \
    elastic/elasticsearch:7.12.1
```

```
docker run \
    -d \
    -p 9202:9202 \
    -p 9302:9302 \
    -v /data/container/elasticsearch/elasticsearch_node03:/usr/share/elasticsearch \
    --name elasticsearch_node03 \
    elastic/elasticsearch:7.12.1
```

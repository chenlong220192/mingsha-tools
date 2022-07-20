- docker run
```
docker run -d \
  -p 3000:3000 \
  -e GF_SECURITY_ADMIN_PASSWORD=123456 \
  -e "GF_INSTALL_PLUGINS=redis-datasource" \
  -v /data/containers/grafana:/usr/share/grafana \
  --name grafana \
  grafana/grafana:8.5.0-51896pre
```
- ⚠️注意：
- 预先将目标目录拷贝至本机：`docker cp grafana:/usr/share/grafana /data/containers/`
- 安装插件 -e "GF_INSTALL_PLUGINS=redis-datasource"

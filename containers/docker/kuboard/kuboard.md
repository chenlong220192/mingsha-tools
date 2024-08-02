- docker run

v3
```
docker run \
  -d \
  --restart=unless-stopped \
  -p 8085:80/tcp \
  -p 10081:10081/udp \
  -p 10081:10081/tcp \
  -e KUBOARD_ENDPOINT="http://10.8.0.1:8085" \
  -e KUBOARD_AGENT_SERVER_UDP_PORT="10081" \
  -e KUBOARD_AGENT_SERVER_TCP_PORT="10081" \
  -e KUBOARD_DISABLE_AUDIT=true \
  -v /data/containers/kuboard-data:/data \
  --memory 1024m \
  --name=kuboard \
  swr.cn-east-2.myhuaweicloud.com/kuboard/kuboard:v3.5.2.7
```

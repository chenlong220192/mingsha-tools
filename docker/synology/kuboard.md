- docker run
```
docker run \
  -d \
  -p 0.0.0.0:8085:80/tcp \
  -p 0.0.0.0:10081:10081/tcp \
  -e KUBOARD_ENDPOINT="http://10.0.0.9:8085" \
  -e KUBOARD_AGENT_SERVER_TCP_PORT="10081" \
  -v /volume1/docker/kuboard-data:/data \
  --memory 256m \
  --restart=no \
  --name=kuboard \
  swr.cn-east-2.myhuaweicloud.com/kuboard/kuboard:v3
```

- docker run
```
docker run -d \
  --privileged \
  -p 8084:80/tcp \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v /volume1/docker/kuboard-spray-data:/data \
  --memory 512m \
  --restart=no \
  --name=kuboard-spray \
  swr.cn-east-2.myhuaweicloud.com/kuboard/kuboard-spray:latest-amd64
```

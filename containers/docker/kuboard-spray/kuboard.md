- docker run
```
docker run \
  -d \
  --restart=unless-stopped \
  -p 0.0.0.0:8084:80/tcp \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v /data/containers/kuboard-spray-data:/data \
  --memory 256m \
  --name=kuboard-spray \
  swr.cn-east-2.myhuaweicloud.com/kuboard/kuboard-spray:latest-amd64
```

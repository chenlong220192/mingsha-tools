- docker run
```
docker run \
    -d \
    -p 2368:2368 \
    -v /volume1/docker/ghost:/var/lib/ghost \
    -e url=http://10.0.0.9:2368/ \
    -e NODE_ENV=production \
    --restart=unless-stopped \
    --memory 256m \
    --name ghost \
    ghost:alpine
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp ghost:/var/lib/ghost/ /volume1/docker/ghost`

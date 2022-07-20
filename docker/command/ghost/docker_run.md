- docker run
```
docker run \
    -d \
    -p 2368:2368 \
    -v /data/docker/ghost/:/var/lib/ghost/ \
    -e url=http://localhost:2368/ \
    -e NODE_ENV=production \
    --name ghost \
    ghost:alpine
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp ghost:/var/lib/ghost/ /data/docker/ghost`

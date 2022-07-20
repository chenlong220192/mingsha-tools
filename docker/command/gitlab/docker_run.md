- docker run
```
docker run \
    -d \
    -p 80:80 \
    -p 443:443 \
    -p 22:22 \
    -v /data/container/gitlab/config:/etc/gitlab \
    -v /data/container/gitlab/log:/var/log/gitlab \
    -v /data/container/gitlab/data:/var/opt/gitlab \
    --name gitlab \
    gitlab/gitlab-ce:14.0.8-ce.0
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp gitlab:/etc/gitlab /data/container/gitlab/config`
  - `docker cp gitlab:/var/log/gitlab /data/container/gitlab/log`
  - `docker cp gitlab:/var/opt/gitlab /data/container/gitlab/data`

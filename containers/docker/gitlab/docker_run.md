- docker run
```
docker run \
    -d \
    -p 80:80 \
    -p 443:443 \
    -p 22:22 \
    -v /data/containers/gitlab/config:/etc/gitlab \
    -v /data/containers/gitlab/log:/var/log/gitlab \
    -v /data/containers/gitlab/data:/var/opt/gitlab \
    --name gitlab \
    gitlab/gitlab-ce:16.10.0-ce.0
```
- ⚠️注意：
- 预先将目标目录拷贝至本机
  - `docker cp gitlab:/etc/gitlab /data/containers/gitlab/config`
  - `docker cp gitlab:/var/log/gitlab /data/containers/gitlab/log`
  - `docker cp gitlab:/var/opt/gitlab /data/containers/gitlab/data`

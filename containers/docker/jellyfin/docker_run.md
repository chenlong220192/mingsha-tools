- docker run
```
docker run \
    -d \
    -p 8096:8096 \
    -v /data/containers/jellyfin/config:/config \
    -v /data/containers/jellyfin/media:/media \
    -v /data/containers/jellyfin/cache:/cache \
    --name jellyfin \
    jellyfin/jellyfin:latest
```

- 中文乱码问题 https://blog.lishun.me/docker-jellyfin-chinese-fonts
apt update & apt install fonts-noto-cjk-extra

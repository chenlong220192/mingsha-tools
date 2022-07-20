- docker run
```
docker run \
    -d \
    -p 8096:8096 \
    -v /volume1/docker/jellyfin/config:/config \
    -v /volume1/docker/jellyfin/cache:/cache \
    -v /volume1/Passport:/media \
    --name jellyfin \
    --restart=always \
    --memory 2048m \
    jellyfin/jellyfin:latest
```

- 中文乱码问题 https://blog.lishun.me/docker-jellyfin-chinese-fonts
apt update & apt install fonts-noto-cjk-extra

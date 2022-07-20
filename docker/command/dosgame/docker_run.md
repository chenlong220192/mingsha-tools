- docker run
```
docker run \
    -d \
    --name dosgame \
    -p 262:262 \
    -v /data/docker/dosgame/games:/app/static/games \
    oldiy/dosgame-web-docker:latest
```

- 需要先将`/app/static/games`拷贝到`/data/docker/dosgame/games`文件中

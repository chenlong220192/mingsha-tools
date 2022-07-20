- nginx-downloads
```
  docker run \
      -d \
      -p 9011:80 \
      -v /data/containers/nginx-downloads/resources:/home/resources \
      -v /data/containers/nginx-downloads/conf.d:/etc/nginx/conf.d \
      --restart always \
      --memory 256m \
      --memory-swappiness 0 \
      --memory-reservation 64m \
      --oom-kill-disable=false \
      --name nginx-downloads \
      nginx:1.23.0-alpine
```

***

- ⚠️参考：https://blog.csdn.net/wugenqiang/article/details/86513257
- ⚠️参考：https://www.cnblogs.com/weifeng1463/p/9314154.html

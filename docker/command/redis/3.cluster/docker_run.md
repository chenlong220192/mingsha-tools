- docker run
```
docker run -d -p 9000:9000 -p 19000:19000 -v /data/container/redis/6.2.1/cluster/9000:/data  /data/redis.conf --memory 32m --name redis-cluster-9000 redis:6.2.7-alpine
docker run -d -p 9001:9001 -p 19001:19001 -v /data/container/redis/6.2.1/cluster/9001:/data  /data/redis.conf --memory 32m --name redis-cluster-9001 redis:6.2.7-alpine
docker run -d -p 9002:9002 -p 19002:19002 -v /data/container/redis/6.2.1/cluster/9002:/data  /data/redis.conf --memory 32m --name redis-cluster-9002 redis:6.2.7-alpine
docker run -d -p 9003:9003 -p 19003:19003 -v /data/container/redis/6.2.1/cluster/9003:/data  /data/redis.conf --memory 32m --name redis-cluster-9003 redis:6.2.7-alpine
docker run -d -p 9004:9004 -p 19004:19004 -v /data/container/redis/6.2.1/cluster/9004:/data  /data/redis.conf --memory 32m --name redis-cluster-9004 redis:6.2.7-alpine
docker run -d -p 9005:9005 -p 19005:19005 -v /data/container/redis/6.2.1/cluster/9005:/data  /data/redis.conf --memory 32m --name redis-cluster-9005 redis:6.2.7-alpine
```

- 创建集群，进入任意redis容器`docker exec -it redis-container-name /bin/bash`执行以下命令。
```
/usr/local/bin/redis-cli --cluster create 127.0.0.1:9000 127.0.0.1:9001 127.0.0.1:9002 127.0.0.1:9003 127.0.0.1:9004 127.0.0.1:9005 --cluster-replicas 1
```

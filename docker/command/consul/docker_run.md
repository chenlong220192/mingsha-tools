- docker run
```
docker run -d -it \
    --name consul \
    -p 8300:8300 \
    -v /data/containers/consul/dc1:/consul/data \
    -e CONSUL_BIND_INTERFACE=eth0 \
    consul:1.9.14
```
- 加入新节点
```
docker run -d --name consul_agent01 -e CONSUL_BIND_INTERFACE=eth0 -v /data/containers/consul/agent01:/consul/data consul:1.9.14 agent -dev -join=172.17.0.4
```
```
docker run -d --name consul_agent02 -e CONSUL_BIND_INTERFACE=eth0 -v /data/containers/consul/agent02:/consul/data consul:1.9.14 agent -dev -join=172.17.0.4
```

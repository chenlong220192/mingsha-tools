- nameserver
```
docker run -d --name rocketmq-namesrv-0 \
    -p 9876:9876 \
    -v /data/containers/rocketmq/namesrv-0/logs:/home/rocketmq/logs \
    -v /data/containers/rocketmq/namesrv-0/store:/home/rocketmq/store \
    apache/rocketmq:5.1.0-alpine ./mqnamesrv
```
```
docker run -d --name rocketmq-namesrv-1 \
    -p 9877:9876 \
    -v /data/containers/rocketmq/namesrv-1/logs:/home/rocketmq/logs \
    -v /data/containers/rocketmq/namesrv-1/store:/home/rocketmq/store \
    apache/rocketmq:5.1.0-alpine ./mqnamesrv
```
```
docker run -d --name rocketmq-namesrv-2 \
    -p 9878:9876 \
    -v /data/containers/rocketmq/namesrv-2/logs:/home/rocketmq/logs \
    -v /data/containers/rocketmq/namesrv-2/store:/home/rocketmq/store \
    apache/rocketmq:5.1.0-alpine ./mqnamesrv
```

- borker
```
docker run -d --name rocketmq-broker-n0 \
    --net=host \
    -v /data/containers/rocketmq/broker-n0/logs:/home/rocketmq/logs \
    -v /data/containers/rocketmq/broker-n0/store:/home/rocketmq/store \
    -v /data/containers/rocketmq/broker-n0/conf:/home/rocketmq/rocketmq-5.1.0/conf \
    apache/rocketmq:5.1.0-alpine sh mqbroker -c ../conf/dledger/broker-n0.conf
```
```
docker run -d --name rocketmq-broker-n1 \
    --net=host \
    -v /data/containers/rocketmq/broker-n1/logs:/home/rocketmq/logs \
    -v /data/containers/rocketmq/broker-n1/store:/home/rocketmq/store \
    -v /data/containers/rocketmq/broker-n1/conf:/home/rocketmq/rocketmq-5.1.0/conf \
    apache/rocketmq:5.1.0-alpine sh mqbroker -c ../conf/dledger/broker-n1.conf
```
```
docker run -d --name rocketmq-broker-n2 \
    --net=host \
    -v /data/containers/rocketmq/broker-n2/logs:/home/rocketmq/logs \
    -v /data/containers/rocketmq/broker-n2/store:/home/rocketmq/store \
    -v /data/containers/rocketmq/broker-n2/conf:/home/rocketmq/rocketmq-5.1.0/conf \
    apache/rocketmq:5.1.0-alpine sh mqbroker -c ../conf/dledger/broker-n2.conf
```

- dashboard
```
docker run -d --name rocketmq-dashboard --net=host -e "JAVA_OPTS=-Drocketmq.namesrv.addr=127.0.0.1:9876" apacherocketmq/rocketmq-dashboard:latest
```
- docker run

- jenkins
```
docker run \
    -d \
    -p 8080:8080 \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v $(which docker):/usr/bin/docker \
    -v /data/containers/jenkins:/var/jenkins_home \
    --name jenkins \
    jenkins/jenkins:2.380-alpine
```

- network
```
docker network create --subnet 10.0.0.0/24 --ip-range 10.0.0.254/24 jenkins-net
```
- jenkins
```
docker run \
    -d \
    -p 127.0.0.1:10010:8080 \
    -p 127.0.0.1:10011:50000 \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v $(which docker):/usr/bin/docker \
    -v /data/container/jenkins:/var/jenkins_home \
    --network jenkins-net \
    --ip 10.0.0.2 \
    --name jenkins \
    jenkins/jenkins:2.380-alpine
```
- slave-01
```
docker run \
    -d \
    -p 127.0.0.1:1022:22 \
    --network jenkins-net \
    --ip 10.0.0.3 \
    --name centos7-sshd-jenkins-agent-01 \
    local/centos7:sshd
```
- slave-02
```
docker run \
    -d \
    -p 127.0.0.1:1023:22 \
    --network jenkins-net \
    --ip 10.0.0.5 \
    --name centos7-sshd-jenkins-agent-02 \
    local/centos7:sshd
```

***
- `-v /var/run/docker.sock:/var/run/docker.sock` 将宿主机docker.sock映射到容器内。
- `-v $(which docker):/usr/bin/docker`将宿主机docker程序映射至jenkins容器内。

- 权限
`chown -R 1000 /data/containers/jenkins`

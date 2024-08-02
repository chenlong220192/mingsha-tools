- sonarqube最新版本
```
docker run \
      -d \
      -it \
      -p 9002:9000 \
      -v /data/container/sonarqube/:/opt/sonarqube/ \
      --name sonarqube \
      sonarqube:latest
```

- sonarqube7.8社区版
```
docker run \
      -d \
      -it \
      -p 9003:9000 \
      -v /data/container/sonarqube-7_8-community/:/opt/sonarqube/ \
      --name sonarqube-7_8-community \
      sonarqube:7.8-community
```

***

- 默认账号密码：`admin/admin`
- 切换数据库可以在`conf/sonar.properties`文件配置
- ⚠️注意：需要提前将以上目录拷贝到本地
  - 例：`docker cp sonarqube:/opt/sonarqube /data/container/sonarqube`

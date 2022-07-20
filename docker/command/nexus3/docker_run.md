- docker run
```
docker run \
    -d \
    -p 8081:8081 \
    -p 8082:8082 \
    -p 8083:8083 \
    -v /data/containers/nexus3:/nexus-data \
    --name nexus3 \
    --restart=always \
    sonatype/nexus3:3.40.1
```

- 权限
`chown -R 200 /data/containers/nexus3`

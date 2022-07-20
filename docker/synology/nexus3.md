- docker run
```
docker run \
    -d \
    -p 8081:8081 \
    -p 8082:8082 \
    -p 8083:8083 \
    -v /volume1/docker/nexus3:/nexus-data \
    --name nexus3 \
    --memory 4096m \
    --restart=always \
    sonatype/nexus3:3.40.1
```

- 权限
`chown -R 200 /volume1/docker/nexus3`

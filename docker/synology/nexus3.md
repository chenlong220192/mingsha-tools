- docker run
```
docker run \
    -d \
    -p 8081:8081 \
    -p 8082:8082 \
    -p 8083:8083 \
    -v /volume1/docker/nexus3:/nexus-data \
    --memory 1536m \
    --restart=no \
    --name nexus3 \
    sonatype/nexus3:3.53.0
```

- 权限
`chown -R 200 /volume1/docker/nexus3`

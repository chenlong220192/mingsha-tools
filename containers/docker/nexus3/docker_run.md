- docker run
```
docker run \
    -d \
    --restart=unless-stopped \
    --ulimit nofile=65536:65536 \
    -p 0.0.0.0:8081:8081/tcp \
    -p 0.0.0.0:5555:8082/tcp \
    -p 0.0.0.0:8083:8083/tcp \
    -e INSTALL4J_ADD_VM_PARAMS="-Xms256M -XX:MaxDirectMemorySize=2048M" \
    -v /data/containers/nexus3:/nexus-data \
    --memory 2048m \
    --name nexus3 \
    sonatype/nexus3:3.69.0
```

- 权限
`chown -R 200 /data/containers/nexus3`

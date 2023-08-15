- nfs
```
  docker run \
    -d \
    -p 0.0.0.0:2049:2049 \
    --privileged \
    -v /data/containers/nfs-data:/data \
    -e SHARED_DIRECTORY=/data \
    --name nfs \
    itsthenetwork/nfs-server-alpine:latest
```

***

- ⚠️参考：https://github.com/openebs/dynamic-nfs-provisioner/tree/develop/nfs-server-container

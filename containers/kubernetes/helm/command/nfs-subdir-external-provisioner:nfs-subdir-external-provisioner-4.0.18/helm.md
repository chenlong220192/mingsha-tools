-
```
helm upgrade --install \
  --create-namespace nfs-subdir-external-provisioner \
  --namespace nfs-subdir-external-provisioner \
  --version 4.0.18 \
  ./chart/nfs-subdir-external-provisioner:nfs-subdir-external-provisioner-4.0.18
```

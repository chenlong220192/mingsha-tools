-
```
helm upgrade --install \
  --create-namespace nfs-subdir-external-provisioner \
  --namespace nfs-subdir-external-provisioner \
  --version 4.0.16 \
  ./chart/choerodon:nfs-subdir-external-provisioner-4.0.16
```

-
```
helm upgrade --install \
  --create-namespace hostpath-provisioner \
  --namespace hostpath-provisioner \
  --version 0.2.13 \
  ./chart/rimusz:hostpath-provisioner-0.2.13
```

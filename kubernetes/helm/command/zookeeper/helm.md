-
```
helm upgrade --install \
  --create-namespace zookeeper \
  --namespace zookeeper \
  --version 11.3.1 \
  ./chart/bitnami:zookeeper-11.3.1
```

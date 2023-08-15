-
```
helm upgrade --install \
  --create-namespace redis-cluster \
  --namespace redis \
  --version 8.4.4 \
  ./chart/bitnami:redis-cluster-8.4.4
```

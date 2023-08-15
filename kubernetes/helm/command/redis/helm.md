-
```
helm upgrade --install \
  --create-namespace redis \
  --namespace redis \
  --version 17.10.1 \
  ./chart/bitnami:redis-17.10.1
```

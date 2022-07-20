-
```
helm upgrade --install \
  --create-namespace redis \
  --namespace redis \
  --version 15.6.0 \
  ./chart/bitnami:redis-15.6.0
```

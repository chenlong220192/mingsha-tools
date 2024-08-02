-
```
helm upgrade --install \
  --create-namespace redis \
  --namespace redis \
  --version 19.6.1 \
  ./chart/bitnami:redis-19.6.1
```

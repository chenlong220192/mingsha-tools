-
```
helm upgrade --install \
  --create-namespace elasticsearch \
  --namespace elasticsearch \
  --version 19.6.0 \
  ./chart/bitnami:elasticsearch-19.6.0
```

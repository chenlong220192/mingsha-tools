-
```
helm upgrade --install \
  --create-namespace elasticsearch \
  --namespace elasticsearch \
  --version 17.5.5 \
  ./chart/bitnami:elasticsearch-17.5.5
```

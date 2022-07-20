-
```
helm upgrade --install \
  --create-namespace consul \
  --namespace consul \
  --version 10.2.3 \
  ./chart/bitnami:consul-10.2.3
```

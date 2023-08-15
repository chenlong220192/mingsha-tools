-
```
helm upgrade --install \
  --create-namespace consul \
  --namespace consul \
  --version 10.10.2 \
  ./chart/bitnami:consul-10.10.2
```

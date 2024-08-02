-
```
helm upgrade --install \
  --create-namespace postgresql \
  --namespace postgresql \
  --version 15.5.10 \
  ./chart/bitnami:postgresql-15.5.10
```

-
```
helm upgrade --install \
  --create-namespace mysql \
  --namespace mysql \
  --version 9.7.2 \
  ./chart/bitnami:mysql-9.7.2
```

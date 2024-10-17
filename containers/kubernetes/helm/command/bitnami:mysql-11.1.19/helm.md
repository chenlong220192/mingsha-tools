-
```
helm upgrade --install \
  --create-namespace mysql \
  --namespace mysql \
  --version 11.1.19 \
  ./chart/bitnami:mysql-11.1.19
```

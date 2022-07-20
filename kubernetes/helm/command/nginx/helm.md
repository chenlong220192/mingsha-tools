-
```
helm upgrade --install \
  --create-namespace nginx \
  --namespace nginx \
  --version 12.0.5 \
  ./chart/bitnami:nginx-12.0.5
```

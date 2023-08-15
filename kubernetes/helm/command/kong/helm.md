-
```
helm upgrade --install \
  --create-namespace kong \
  --namespace kong \
  --version 2.19.0 \
  ./chart/kong:kong-2.19.0
```

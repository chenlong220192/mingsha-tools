-
```
helm upgrade --install \
  --create-namespace metrics-server \
  --namespace metrics-server \
  --version 3.8.2 \
  ./chart/metrics-server:metrics-server-3.8.2
```

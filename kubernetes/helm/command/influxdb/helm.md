-
```
helm upgrade --install \
  --create-namespace influxdb \
  --namespace influxdb \
  --version 5.7.0 \
  ./chart/bitnami:influxdb-5.7.0
```

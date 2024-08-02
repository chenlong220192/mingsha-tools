-
```
helm upgrade --install \
  --create-namespace prometheus-blackbox-exporter \
  --namespace prometheus \
  --version 7.7.0 \
  ./chart/prometheus-community:prometheus-blackbox-exporter-7.7.0
```

-
```
helm upgrade --install \
  --create-namespace opentelemetry-collector \
  --namespace opentelemetry-collector \
  --version 0.66.4 \
  ./chart/open-telemetry:opentelemetry-collector-0.66.4
```

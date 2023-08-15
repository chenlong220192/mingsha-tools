-
```
helm upgrade --install \
  --create-namespace grafana \
  --namespace grafana \
  --version 6.55.1 \
  ./chart/grafana:grafana-6.55.1
```

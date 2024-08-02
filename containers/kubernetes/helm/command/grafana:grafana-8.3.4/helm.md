-
```
helm upgrade --install \
  --create-namespace grafana \
  --namespace grafana \
  --version 8.3.4 \
  ./chart/grafana:grafana-8.3.4
```

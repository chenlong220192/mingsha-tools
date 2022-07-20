-
```
helm upgrade --install \
  --create-namespace grafana \
  --namespace grafana \
  --version 6.31.1 \
  ./chart/grafana:grafana-6.31.1
```

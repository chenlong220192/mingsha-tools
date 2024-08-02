-
```
helm upgrade --install \
  --create-namespace prometheus \
  --namespace prometheus \
  --version 15.9.1 \
  --set nodeExporter.hostRootfs=false \
  ./chart/prometheus-community:prometheus-15.9.1
```
- ⚠️注意：
- `--set nodeExporter.hostRootfs=false` 避免Prometheus挂载`/`到宿主机的`/`

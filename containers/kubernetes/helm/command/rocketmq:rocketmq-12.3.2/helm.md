-
```
helm upgrade --install \
  --create-namespace rocketmq \
  --namespace rocketmq \
  --set dashboard.enabled="true" \
  --version 12.3.2 \
  ./chart/rocketmq:rocketmq-12.3.2
```

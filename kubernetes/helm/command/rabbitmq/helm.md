-
```
helm upgrade --install \
  --create-namespace rabbitmq \
  --namespace rabbitmq \
  --version 11.13.0 \
  ./chart/bitnami:rabbitmq-11.13.0
```

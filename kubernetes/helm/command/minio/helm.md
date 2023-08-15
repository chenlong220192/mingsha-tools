-
```
helm upgrade --install \
  --create-namespace minio \
  --namespace minio \
  --version 12.6.9 \
  ./chart/bitnami:minio-12.6.9
```

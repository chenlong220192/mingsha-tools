-
```
helm upgrade --install \
  --create-namespace nginx-ingress \
  --namespace nginx-ingress \
  --version 0.14.0 \
  ./chart/nginx:nginx-ingress-0.14.0
```

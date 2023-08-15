-
```
helm upgrade --install \
  --create-namespace nginx-ingress-controller \
  --namespace nginx-ingress-controller \
  --version 9.5.1 \
  ./chart/bitnami:nginx-ingress-controller-9.5.1
```

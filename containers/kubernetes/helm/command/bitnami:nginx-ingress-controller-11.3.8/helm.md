-
```
helm upgrade --install \
  --create-namespace nginx-ingress-controller \
  --namespace nginx-ingress-controller \
  --version 11.3.8 \
  ./chart/bitnami:nginx-ingress-controller-11.3.8
```

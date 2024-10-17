-
```
helm upgrade --install \
  --create-namespace nginx-ingress-controller \
  --namespace nginx-ingress-controller \
  --version 11.4.4 \
  ./chart/bitnami:nginx-ingress-controller-11.4.4
```

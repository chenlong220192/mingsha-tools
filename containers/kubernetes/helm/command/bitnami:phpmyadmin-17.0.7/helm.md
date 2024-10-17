-
```
helm upgrade --install \
  --create-namespace phpmyadmin \
  --namespace phpmyadmin \
  --version 17.0.7 \
  ./chart/bitnami:phpmyadmin-17.0.7
```

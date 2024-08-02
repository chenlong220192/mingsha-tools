-
```
helm upgrade --install \
  --create-namespace sonarqube \
  --namespace sonarqube \
  --version 5.2.7 \
  ./chart/bitnami:sonarqube-5.2.7
```

-
```
helm upgrade --install \
  --create-namespace jenkins \
  --namespace jenkins \
  --version 4.1.11 \
  ./chart/jenkinsci:jenkins-4.1.11
```

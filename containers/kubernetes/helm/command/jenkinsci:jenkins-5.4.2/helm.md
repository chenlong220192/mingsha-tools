-
```
helm upgrade --install \
  --create-namespace jenkins \
  --namespace jenkins \
  --version 5.4.2 \
  ./chart/jenkinsci:jenkins-5.4.2
```

-
```
helm upgrade --install \
  --create-namespace jenkins \
  --namespace jenkins \
  --version 5.7.5 \
  ./chart/jenkinsci:jenkins-5.7.5
```

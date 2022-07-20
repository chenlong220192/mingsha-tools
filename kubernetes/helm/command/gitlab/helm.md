-
```
helm upgrade --install \
  --create-namespace gitlab \
  --namespace gitlab \
  --version 6.0.3 \
  --set certmanager-issuer.email=chenlong220192@gmail.com \
  ./chart/gitlab:gitlab-6.0.3
```

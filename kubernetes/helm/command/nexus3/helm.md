-
```
helm upgrade --install \
  --create-namespace nexus3 \
  --namespace nexus3 \
  --version 39.0.1 \
  ./chart/sonatype:nexus-repository-manager-39.0.1
```

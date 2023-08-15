-
```
helm upgrade --install \
  --create-namespace sonatype \
  --namespace sonatype \
  --version 52.0.0 \
  ./chart/sonatype:nexus-repository-manager-52.0.0
```

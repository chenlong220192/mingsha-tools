-
```
helm upgrade --install \
  --create-namespace ollama \
  --namespace ollama \
  --version 0.60.0 \
  ./chart/ollama-helm:ollama-0.60.0
```

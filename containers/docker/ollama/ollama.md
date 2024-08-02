- docker run
```
docker run -d \
  --restart=unless-stopped \
  -p 11434:11434 \
  -v /data/containers/ollama:/root/.ollama \
  -e "OPENAI_LANGUAGE=zh_CN" \
  --memory 8192m \
  --name ollama \
  ollama/ollama:latest
```

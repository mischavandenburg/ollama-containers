# Prebuilt Ollama containers

```bash
# log in to ghcr
echo $GITHUB_TOKEN |  docker login ghcr.io -u mischavandenburg --password-stdin

# cd into directory and tag based on directory name
MODEL_NAME=$(basename "$PWD") && docker buildx build --platform linux/amd64 -t ghcr.io/mischavandenburg/ollama-containers/$MODEL_NAME . --push
```

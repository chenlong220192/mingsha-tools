- jenkins
```
docker run \
    -d \
    -p 0.0.0.0:8080:8080 \
    -v /volume1/docker/jenkins:/var/jenkins_home \
    --memory 1024m \
    --restart=no \
    --name jenkins \
    jenkins/jenkins:2.403-alpine
```

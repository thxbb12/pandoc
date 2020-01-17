# What is it?

A Dockerfile to create a pandoc docker image.

## Build the image
```
docker build . -t pandoc:2.6
```

## Setup credentials
```
docker login
```

## Push the image to DockerHub
```
docker tag pandoc:2.6 thxbb12/pandoc:2.6
docker push thxbb12/pandoc:2.6
```

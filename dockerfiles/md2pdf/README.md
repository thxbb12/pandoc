## What is it?

A Dockerfile to create a md2pdf Docker image.
This image allows you to convert markdown files (.md) to:

- Slides (using pandoc/beamer)
- Practical lab documents (using pandoc/latex)

Please note that this image uses the thxbb12/pandoc:2.6 image.

## Build the image
```
docker build . -t md2pdf
```

## Setup credentials
```
docker login
```

## Push the image to DockerHub
```
docker tag md2pdf thxbb12/md2pdf
docker push thxbb12/md2pdf
```

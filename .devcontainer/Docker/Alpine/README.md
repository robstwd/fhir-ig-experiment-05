# Alpine-based Dockerfile notes

## Image source
From Docker hub official Debian image page: https://hub.docker.com/_/openjdk

However, this image has been officially deprecated

## Alternative

One option would be create an image based on bare Alpine, like this

```Dockerfile
FROM alpine:3.17

RUN apk --no-cache update && \
    apk --no-cache upgrade && \
    apk --no-cache add \
       openjdk11-jre-headless \
       ruby \
       bash \
       curl \
       git \
       jekyll \
       fontconfig \
       ttf-dejavu
```

However, this has not managed to work with a variety of modifications.

Transitioned to using Debian as the base instead.
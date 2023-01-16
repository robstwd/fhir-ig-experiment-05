FROM openjdk:19-jdk-alpine

RUN apk  --no-cache update && \
    apk  --no-cache upgrade && \
    apk  --no-cache add \
       ruby \
       bash \
       curl \
       git \
       jekyll \
       freetype

WORKDIR /workspaces/fhir-ig-experiment-05

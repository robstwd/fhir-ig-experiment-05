FROM openjdk:19-jdk-alpine

RUN apk update && \
    apk upgrade && \
    apk add \
       ruby \
       bash \
       curl \
       git \
       jekyll \
       freetype \       
    rm -rf /var/cache/apk/*

WORKDIR /workspaces/fhir-ig-experiment-05

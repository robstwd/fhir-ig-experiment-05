FROM openjdk:19-jdk-alpine

RUN apk update && \
    apk upgrade && \
    apk add \
       ruby \
       git \
       jekyll \
    rm -rf /var/cache/apk/*
    
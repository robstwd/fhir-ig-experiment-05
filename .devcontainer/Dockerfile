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

RUN git submodule update --init --recursive --remote && \
    mkdir input-cache && \
    wget -q https://github.com/HL7/fhir-ig-publisher/releases/latest/download/publisher.jar -O input-cache/publisher.jar

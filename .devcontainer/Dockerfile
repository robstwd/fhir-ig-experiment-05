FROM openjdk:19-jdk-alpine

RUN apk update && \
    apk upgrade && \
    apk add \
       bash \
       ruby \
       ruby-jekyll \
       jekyll \
    rm -rf /var/cache/apk/*

CMD /bin/bash
    
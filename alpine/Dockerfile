FROM alpine:latest

RUN echo "@community http://dl-4.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories && \
    echo "@testing http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk update && apk upgrade && \
    apk add stress --update-cache --repository http://dl-8.alpinelinux.org/alpine/edge/testing/ --allow-untrusted

ENTRYPOINT ["stress"]

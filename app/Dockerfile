FROM alpine:latest

LABEL maintainer "Hidetoshi Imai <hidepin@gmail.com>"

RUN apk add --update \
    openssl-dev \
    libffi-dev \
    musl-dev \
    python-dev \
    gcc \
    py-pip \
    sshpass \
    tzdata && \
    pip install ansible==2.2.0.0 && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    echo "Asia/Tokyo" >  /etc/timezone

RUN mkdir -p /playbook
WORKDIR /playbook

CMD ["ansible", "--version"]

FROM jamiehewland/alpine-pypy:3-6.0.0-alpine3.7
LABEL maintainer "kingzeus <kingzeus@gmail.com>"

#RUN  echo "http://nl.alpinelinux.org/alpine/edge/testing">>/etc/apk/repositories
RUN apk update
RUN apk add curl libxml2-dev libxslt-dev libffi-dev gcc musl-dev libgcc openssl-dev


RUN pip3 install scrapy


VOLUME /data

#CMD ["sh"]
ENTRYPOINT scrapy;pypy3
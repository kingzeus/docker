FROM alpine:latest
MAINTAINER WangXian <xian366@126.com>

WORKDIR /app
VOLUME /app
COPY startup.sh /startup.sh

RUN apk add --update mysql mysql-client && rm -f /var/cache/apk/*
COPY my.cnf /etc/mysql/my.cnf

RUN ["chmod", "+x", "/startup.sh"]

EXPOSE 3306

# exectute start up script
CMD ["/startup.sh"]

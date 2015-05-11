FROM ubuntu:trusty

MAINTAINER Johann Saunier <johann_27@hotmail.fr>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y php5-cli php5-curl && apt-get clean
RUN echo "date.timezone = \"Europe/Paris\"" >> /etc/php5/cli/php.ini
RUN echo "memory_limit = 512M" >> /etc/php5/cli/php.ini

VOLUME ["/app"]
WORKDIR /app

CMD ["-"]

ENTRYPOINT ["php"]
FROM php:5.6-cli

MAINTAINER Johann Saunier <johann_27@hotmail.fr>

RUN DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get upgrade -y 
RUN apt-get install -y zlib1g-dev git mercurial subversion --no-install-recommends && rm -r /var/lib/apt/lists/*
RUN docker-php-ext-install zip
RUN echo "memory_limit=1024M" > /usr/local/etc/php/conf.d/memory-limit.ini

ENV COMPOSER_HOME /root/composer

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer --version=1.0.0-alpha10

RUN mkdir -p /root/composer
ADD auth.json /root/composer/auth.json

RUN php --version
RUN composer --version

VOLUME ["/app"]
WORKDIR /app

CMD ["-"]

ENTRYPOINT ["composer", "--ansi"]

FROM maxexcloo/nginx-php:latest
MAINTAINER Patrik Votocek <patrik@votocek.cz>
RUN apt-get update
RUN apt-get install -y git
RUN wget -O /data/composer.phar "https://getcomposer.org/composer.phar"
RUN sed -i "s,pcre_jit on;,,g" /etc/nginx/nginx.conf

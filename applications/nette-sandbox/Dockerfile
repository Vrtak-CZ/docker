FROM vrtakcz/nginx-php-composer:latest
MAINTAINER Patrik Votocek <patrik@votocek.cz>
RUN git clone https://github.com/nette/sandbox.git /data/http
RUN git --work-tree=/data/http --git-dir=/data/http/.git checkout v2.2
RUN php /data/composer.phar install -d /data/http
RUN sed -i "s,/data/http,/data/http/www,g" /etc/nginx/host.d/default.conf

FROM maxexcloo/debian:latest
MAINTAINER Patrik Votoček <patrik@votocek.cz>
ENV PERCONADB_DB NONE
ENV PERCONADB_USER docker
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys 1C4CBDCDCD2EFD2A
RUN echo "deb http://repo.percona.com/apt wheezy main" > /etc/apt/sources.list.d/perconadb.list
RUN apt-get update
RUN apt-get install -y percona-server-server-5.6 percona-server-client-5.6 libjemalloc1 percona-server-tokudb-5.6
RUN sed -i -e "s/^bind-address/#bind-address/" /etc/mysql/my.cnf
RUN sed -i -e "s/^datadir.*=.*/datadir = \/data/" /etc/mysql/my.cnf
ADD config /config
ADD supervisord.conf /etc/supervisor/conf.d/perconadb.conf
EXPOSE 3306

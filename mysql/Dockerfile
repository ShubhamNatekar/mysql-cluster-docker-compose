FROM mysql:latest
MAINTAINER Shubham Natekar <shubhamnatekar9221@gmail.com>

#VOLUME /var/lib/mysql

COPY cnf/my.cnf /etc/
COPY cnf/mysql-cluster.cnf /etc/
COPY db/init.sql /docker-entrypoint-initdb.d/init.sql

#EXPOSE 3306 33060 2202 1186

#CMD ["mysqld"]


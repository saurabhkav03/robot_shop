FROM mysql

VOLUME [ "/data" ]

ENV MYSQL_ALLOW_EMPTY_PASSWORD=yes \
    MYSQL_DATABASE=cities \
    MYSQL_USER=shipping \
    MYSQL_PASSWORD=secret
    
# change datadir entry in /etc/mysql/my.cnf

COPY mysql/config.sh /root/
RUN /root/config.sh 

COPY mysql/scripts/* /docker-entrypoint-initdb.d/


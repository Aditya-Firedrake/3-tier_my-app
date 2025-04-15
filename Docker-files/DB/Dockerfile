FROM mysql:8.0.33
LABEL "project"="vprofile"
LABEL "author"="aditya"

ENV MYSQL_ROOT_PASWORD="vprobpass"
ENV MYSQL_DATABASE="accounts"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql1
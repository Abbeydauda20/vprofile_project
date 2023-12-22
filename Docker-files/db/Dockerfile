FROM mysql:8.0.33
LABEL "project"="vprofile_project"
LABEL "Author"="Abbeydauda20"

ENV MYSQL_ROOT_PASSWORD="vprodpass"
ENV MYSQL_DATABASE="account"

ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
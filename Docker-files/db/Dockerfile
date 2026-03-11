FROM mysql:8.0.33

LABEL "Project"-"Vprofile"
LABEL "Practise Author"="Parimal"

ENV MYSQL_ROOT_PASSWORD="root123"
ENV MYSQL_DATABASE="accounts"
ENV MYSQL_USER="admin"
ENV MYSQL_PASSWORD="pass123"

COPY *.sql /docker-entrypoint-initdb.d/





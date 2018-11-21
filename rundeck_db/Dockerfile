FROM mysql
ENV MYSQL_DATABASE rundeck
ENV MYSQL_ALLOW_EMPTY_PASSWORD yes
COPY ./sql-scripts/ /docker-entrypoint-initdb.d/

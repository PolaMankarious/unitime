

Pola Magdy Girgis 20236138

Type: Bug Fix

Change Request ID: 1

Priority: Medium

Currently Working on maintainability issues:

2 issues in docker/mysql.Dockerfile and 1 issue in docker/tomcat.Dockerfile

&#x09;2 Replace Add with instruction:

&#x09;	ADD ./doc/mysql/schema.sql /docker-entrypoint-initdb.d/1-schema.sql

&#x09;	ADD ./doc/mysql/woebegon-data.sql /docker-entrypoint-initdb.d/2-data.sql

&#x09;	

&#x09;1 Replace Add with instruction:

&#x09;	ADD web/UniTime.war /usr/local/tomcat/webapps/ROOT.war

&#x09;

&#x09;**COPY is always favored in Dockerfiles over ADD when copying local files. COPY results in less errors.**


Grass BPMN Web Designer
========

Open Source Java based BPMN Web Designer

How to configure the environment:

(1)Download and install Postgres database, the download URL:http://www.postgresql.org/download/

(2)Download and install Tomcat Server Version 6 version, the download URL:http://tomcat.apache.org/tomcat-6.0-doc/index.html

(3)Download and install Eclipse, then import the Grass BPMN Web Designer project

(4)Download and install Python 3.2 version (can't be other version), the download URL:http://www.python.org/download/releases/3.2.5/

(5)Initialize database(only need be done at the first time):
   
   a. Create a new user "poem" and grant all permission to him.
   
   b. Create a new database "poem", owner is the new created user "poem". the script is as following, you also can create it in pgAdmin tool.
   CREATE DATABASE poem
  WITH OWNER = poem
       ENCODING = 'UTF8'
       TABLESPACE = pg_default
       LC_COLLATE = 'English, United States'
       LC_CTYPE = 'English, United States'
       CONNECTION LIMIT = -1;
   
   c. Switch current database to poem, then execute the sql script in gdesigner/poem-jvm/data/database/db_schema.sql

(6)Config the gdesigner/build.properties, you can configue postgres database host name,user name, port and location of postgres database bin directory.

   
(7)In eclipse, go to Grass BPMN Web Designer project (gdesigner), execute "ant rebuild-all" first, then execute "ant deploy-all" to deploy project to tomcat server, 
then start tomcat server.

 (8)In browser, input URL:http://localhost:8080/backend/poem/repository, will open the repository admin page, input URL:http://localhost:8080/oryx/editor, will open 
 oryx editor page. no need login.
  
 
 
 
﻿# cinema-app
## :wrench:	 How to setup :wrench:	

### For connection to database

1. create MySql connection in local Desktop <br/><br/>

2. open file with path

 src/main/resources/db.properties <br/><br/>

3. change lines to 

db.url=jdbc:mysql://YOUR_HOST:YOUR_PORT/cinema?serverTimezone=UTC

db.user=YOUR_USERNAME

db.password=YOUR_PASSWORD <br/><br/>

### For start project 

0. download Tomcat version 9 and Intelij Idea Ultimate

1. click in IDE to Edit Configuration 

2. click Add New Configuration

3. pick Tomcat Server - Local

4. click Configure 

5. in "Tomcat Home" select our downloaded before tomcat 9 and click Ok

6. step to Deployment menu 

7. click add select taxi-service:war exploaded

8. Apply, Ok

9. select in Configuration Tomcat and run <br/><br/>

#### Use guide

for get complitely experience you need to you "Postman" or alternative utils for send post request

for register user, Postman help you with that 

send post request json format email and password to "/register" controller 

example {"email":"YOUR_EMAIL","password":"YOUR_PASSWORD"} <br/><br/>

for login you can use login form: - send request to "/login" <br/><br/>

after authentication
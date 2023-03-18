# cinema-app
 My second java pet project
 
 it`s simple example of movie application
 
 in this application i used spring framework that help me to develop controllers which can recieve post/put/delete requests 
 
 spring security for create authentication with supports several roles 
 
 The project follows the MVC architecture pattern, SOLID principle, exception handling.

The code is well-organized, making it easy to understand and modify

 
 ## Features
Authentication by User
Role User :
- Display all movies | Display all cinema halls | Display avaliable movie sessions | Display all orders | Display user shopping cart 
- Add to user shopping cart movie | Complete order

Role Admin : 

- Display all movies | Display all cinema halls | Display avaliable movie sessions | Display user by email
- create new movie | create new cinema hall | create movie session
- change movie session details


## :rocket:	Involved Technologies::rocket:	

Java

Spring

Spring security

Hibernate

MySql

jdbc

Tomcat


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

### :blue_book: Use guide :blue_book:

for get complitely experience you need to you "Postman" or alternative utils for send post request

for register user, Postman help you with that 

send post request, body in json format, to "/register" url 

<img src="https://i.postimg.cc/R0ZPgwD1/register-user.png" width = "400" >

example {"email":"YOUR_EMAIL","password":"YOUR_PASSWORD"} <br/><br/>

for login you can use login form: - send request to "/login" <br/><br/>

##### after authentication you can use this url:

- get request - "/cinema-halls", "/movies", "/movie-sessions/available" "/orders", "/shopping-carts/by-user"

<img src="https://i.postimg.cc/FKMjfyN9/user-get.png" width = "400" >

- post request - "/orders/complete"

<img src="https://i.postimg.cc/NFdhffmw/user-post.png" width = "200" >

- put request - "/shopping-carts/movie-sessions"

<img src="https://i.postimg.cc/MTstncPt/user-put.png" width = "400" >

if you want to feel like ADMIN you can login - 

"login": "admin@i.ua"

"password": "admin123"

##### Admin role avaliable this url:

- get request - "/cinema-halls/", "/movies/", "/movie-sessions/available", "/users/by-email?email=YOUR_EMAIL"

<img src="https://i.postimg.cc/bvGpdbwN/admin-get.png" width = "500" >

- post request - "/cinema-halls", "/movies", "/movie-sessions"

<img src="https://i.postimg.cc/6qvnHQKf/admin-post.png" width = "800" >

- put request - "/movie-sessions/YOUR_ID" (body = "movieId", "cinemaHallId", "showTime")

<img src="https://i.postimg.cc/nzyvNvCs/admin-put.png" width = "500" >

- delete request - "/movie-sessions/YOUR_ID"

<img src="https://i.postimg.cc/fRdhNs2J/admin-delete.png" width = "200" >

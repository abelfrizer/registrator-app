# Welcome to IQ Registrator

Basically this is for an assessment given to Abel Mapharisa

### pre-assumptions ###

* Healthy internet line
* Docker is working
* Both Git & maven are installed, with a min of JDK8

### Tech Stack ###

* BackEnd: SpringBoot
* UI: Angular 9
* DB: MySQL

# How do I get set up?
Well, the initial plan was to get this working via docker-compose... but unfortunately I couldn't get the ui's Dockerfile to work on time... so humble apologies for the run-around

### Start-up the database ###

* Start-up MySQL database via docker
> `docker container run --name mysqldb -p3308:3306 -e MYSQL_DATABASE='REGISTRATORDB' -e MYSQL_USER='reg_usr' -e MYSQL_PASSWORD='}8{G%hfGg,Dtqk:&' -e MYSQL_ROOT_PASSWORD='P@$$word' -d mysql:8`

### Start-up the service ###

* Clone this project then step into the project directory
 >`git clone git@bitbucket.org:wyzcrew/registrator-app.git`
> `cd registrator-app`
* Pull all dependencies and ensure you have the latest code 
>`git submodule update --init --recursive`
> `git submodule foreach --init --recursive git checkout master` then 
> `git submodule foreach --init --recursive git pull`
* Maven build project
> `mvn clean install`

*  Now run your app ~~via docker-compose~~
> ~~docker-compose up~~
* Go into the service's diretory 
> `cd registrator-service`
*Now run the service 
> `mvn spring-boot:run`
> At the end of this, you will have your application running and accessible via localhost:8080, you can hit the swagger url here, to confirm it's up and running: http://localhost:8080/swagger-ui.html

### Start-up the ui ###
* Go into your ui project ${workingDirectory}/registrator-app/registrator-ui
> `cd registrator-app/registrator-ui`
* Once there, run npm install to ensure all the dependencies are pulled
> `npm install`
* Now run the ui: 
> `npm start`
* At the end of this, you will have the UI running on http://localhost:4200


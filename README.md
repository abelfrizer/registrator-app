# README #

Basically this is for an assessment given to Abel Mapharisa

### pre-assumptions ###

* Healthy internet line
* Docker is working
* Both Git & maven are installed, with a min of JDK8

### Tech Stack ###

* BackEnd: SpringBoot
* UI: Angular 9
* DB: MySQL

### How do I get set up? ###

* Clone this project: `git clone git@bitbucket.org:wyzcrew/registrator-app.git`
* cd into the project: 
`cd registrator-app`
* Pull all dependencies `git submodule update --init --recursive`
* Ensure you have latest code `git submodule foreach --init --recursive git checkout master` then 
`git submodule foreach --init --recursive git pull`
* Maven build project
* `mvn clean install`
* Now run your app
* `docker-compose up`


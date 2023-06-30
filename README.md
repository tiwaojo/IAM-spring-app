# IAM-spring-app

A middleware written in Spring Boot Framework for the Identity and Access Management(IAM) Spring Boot Application for the Computer Security course. Final Report can be viewed [here](Project%20Final%20Report%20CS%20Group%208.pdf).


### Getting started

1. `docker-compose up -d`
2. Run the spring application to create the tables
3. `docker-compose exec postgresqldb bash`
4. `psql -U root -d easy_eng`
5. To see tables: `\dt`, to describe table `\d [name]`
6. exit to exit psql, exit again to exit container
7. stop application before closing docker, FROM NOW WHEN U WANT TO RUN THIS APPLICATION WITHOUT LOSING DATA DO: `docker-compose stop [optional {docker image name}]` (to stop), docker-compose start [optional {docker image name}]

**Note:** you may need to update the address of your database(`spring.datasource.url`) in your [application.properties](forum\src\main\resources\application.properties). You can use `hostname -i` to get the ip address.

### Roles/Permissions
Admin  - edit threads/comments, delete threads/comments, create threads, see list of threads, see comments on a thread, make a comment
Moderator - delete threads/comments, create threads, see list of threads, see comments on a thread, make a comment
Creator - create threads, see list of threads, see comments on a thread, make a comment
Viewer - see list of threads, see comments on a thread, make a comment
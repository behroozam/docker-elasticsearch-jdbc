# Docker ELK stack for Mysql with phpmyadmin

it is a infrastructure for using elasticsearch to index a mysql database with mysql-jdbc driver and logstash plugin aggregate to create event based entry for elasticsearch you can read [this document](https://www.elastic.co/guide/en/logstash/5.6/plugins-filters-aggregate.html#plugins-filters-aggregate) for more information 
i use aggregate to filter records that have same id and diffrent tags 
and collect all in one.

### installation and use 
`rename .env.example to .env`
change .env file as your need 
`docker-compose build`
`docker-compose up -d`
now your mysql and phpmyadmin is ready add your database and change logstash pipline 
lastrun in logstash see your last value that indexed from database and prevent from index whole database again . 
your change will save in data directory in mysql and elasticsearch 



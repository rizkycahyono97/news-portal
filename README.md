# news-portal

## The Problem
1. **Import backup mysql manually**
  ```bash
  docker cp /home/ch4rl0tt3/Downloads/News\ portal\ Project\ in\ PHP\ and\ MySQL/sql\ file/newsportal.sql mysql_db:/newsportal.sql
  SOURCE /newsportal.sql;
2. **install some module in php container**
  ```bash
  apt-get update
  docker-php-ext-install mysqli
  restart container 

## Run The Aplication
1. **run using docker**
  ```bash
  docker-compose up -d


## PHP Development environment
### Introduction
This project will facilitate inbuilt development environment for developers

#### Technology 
 - Docker
 - Docker compose 
 - Nginx
 - PHP 5.6, PHP 7.0, PHP 7.1, PHP 7.2

### Installation:
 1. Clone this project
 1. Copy the file __.env.dist__ to __.env__ and change (LOCAL_SRC) path to your project path
 1. update /etc/hosts file with following line
 __Example:__
 ```bash
 127.0.0.1	php56 php70 php71 php72
 ```
 
#### Env information 

| PHP Version  | Host | 
| ------------- | ------------- |
| PHP 7.2  | http://php72  | 
| PHP 7.1  | http://php71  | 
| PHP 7.0  | http://php70  | 
| PHP 5.6  | http://php56  | 

### Config & Database

DB | Host | User | Password
--- | --- | --- | ---
**PostresSQL** | pgsql | postresql | 
**Mysql** | mysql | root | root

To use the command line clients provided by the containers you can use the following commands:

```bash
# PostgreSQL
docker-compose exec pgsql psql -U postgres

# MySQL
docker-compose exec mysql` mysql -u root -p"root"
```

#### How to browse your projects 

- php 5.6 : http://php56/projectName}/testme.php
- php 7.0 : http://php70/projectName}/testme.php
- php 7.1 : http://php71/{projectName}/testme.php
- php 7.2 : http://php72/{projectName}/testme.php

#### How to execute unit tests
 __Execute Test PHP 7.2:__
 ```bash
 docker-compose exec php-7.2 /bin/bashh
 phpunit
 ```
 
  __Execute Test PHP 7.1:__
  ```bash
  docker-compose exec php-7.1 /bin/bashh
  phpunit
  ```
  
  __Execute Test PHP 7.0:__
  ```bash
   docker-compose exec php-7.0 /bin/bashh
   phpunit
  ```

# Django development work container

## Author

yoshi0518

## Description

Django development work container

## Version

- Python 3.9.2
- Django 3.1
- MySQL 8.0.23
- phpMyAdmin 5.0.4

## How to Use

### Docker

```bash
# Create network
$ docker network create my-network
$ docker network ls

# Build
$ docker-compose build

# Create and launch container
$ docker-compose up -d

# List containers
$ docker-compose ps

# Connect to mysql container
$ docker-compose exec mysql /bin/bash

# Check valid my.conf
$ mysql --help | grep my.cnf
$ cat /etc/my.cnf

# MySQL login
# root/Sys@dm!n01
$ mysql -u root -p
# user/P@ssword01
$ mysql -u user -p

# Variable check(character code)
$ show variables like '%chara%';

# Variable check(collation)
$ show variables like '%colla%';

# Variable check(default authentication)
$ show variables like '%auth%';

# MySQL logout
$ exit

# Connect to django container
$ docker-compose exec django /bin/bash

# Connect to phpmyadmin container
$ docker-compose exec phpmyadmin /bin/bash

# Disconnect from container
$ exit

# Stop container
$ docker-compose down
```

## Link

[Django](http://localhost:8000)

[phpMyAdmin](http://localhost:8080)

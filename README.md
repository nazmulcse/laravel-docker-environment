# laravel-docker-environment
A pretty simplified Docker Compose workflow that sets up a LAMP network of containers for local Laravel development.


## Usage

To get started, make sure you have [Docker installed](https://docs.docker.com/get-docker/) on your system, and then clone this repository.

Next, navigate in your terminal to the directory you cloned this, and spin up the containers for the web server by running `docker-compose up -d`


The following are built for our web server, with their exposed ports detailed:

- **apache** - `:8080`
- **mysql** - `:3306`
- **phpmyadmin** - `:8183`
- **redis port** - `:6379`

Use the following command examples from your project root, modifying them to fit your particular use case.

- `docker-compose exec app composer create-project laravel/laravel .`
- `docker-compose exec app composer update`
- `docker-compose exec app php artisan key:generate`
- `docker-compose exec app npm install` 

Add custom php ini configuration to this file `.docker/php_custom.ini`

## Directory Structure

```
.docker		# Contain docker file. Such as php-apache image, Virtual host file and php custom ini file
.db			# Database folder. 
.docker-compose.yml		# docker compose file
```

## Source


[https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose](https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose)

[https://www.appzcoder.com/dockerize-php-application/](https://www.appzcoder.com/dockerize-php-application/)

[https://dev.to/aschmelyun/crafting-a-better-local-laravel-dev-environment-with-docker-45cj](https://dev.to/aschmelyun/crafting-a-better-local-laravel-dev-environment-with-docker-45cj)

[Best practices for writing Dockerfiles](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)

[Compose file version 3 reference](https://docs.docker.com/compose/compose-file/)



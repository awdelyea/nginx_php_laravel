# Nginx PHP5 Composer Container For Laravel

This is a docker image for running a Laravel project with nginx and php-fpm

## Prerequisites

This docker container expects the following file structure:
```
/Data
|--> /http <laravel app goes here>
|--> /config
|--> /logs
|--> /secure
```

## Installation

```sh
docker build -t awdelyea/php_composer git://github.com/awdelyea/nginx_php_laravel
```

## How To Use

If running this in a dev environment with an already running 'data' container:
```sh
docker run -d --name="nginx-php" -p 8080:80 --volumes-from="data" -it awdelyea/nginx-php-laravel
```

If running standalone:
```sh
docker run -d --name="nginx-php" -p 8080:80 -v <path/to/app>:/data/ -it awdelyea/nginx-php-laravel
```

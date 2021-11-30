# Docker Compose for Nginx and PHP

This repository contains a little `docker-compose` configuration to start a `Nginx and PHP`.

## Details

The following versions are used.

* PHP 8.0 (FPM) - with xdebug 3.1.1, mysqli and pdo
* Nginx latest

## Configuration

The Nginx configuration can be found in `config/nginx/`.

You can also set the following environment variables, for example in the included `.env` file:

| Key | Description |
|-----|-------------|
|APP_NAME|The name used when creating a container.|

## Usage

To use it, simply follow the following steps:

##### Clone this repository.

Clone this repository with the following command: `git clone https://github.com/matejsuchy/php_nginx_xdebug.git`.

##### Start the server.

Start the server using the following command inside the directory you just cloned: `docker-compose up -d --build`.

## Entering the containers

You can use the following command to enter a container:

Where `{CONTAINER_NAME}` is one of:

`docker exec -ti {CONTAINER_NAME} /bin/bash`

* `{APP_NAME}-php`
* `{APP_NAME}-nginx`
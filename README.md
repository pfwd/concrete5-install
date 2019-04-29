# Concrete5 install with Docker

## Specs
- Concrete 5 8.5.1
- MYSQL 8
- PHP 7.2

## Requirements
- Docker
- Docker Machine
- Docker Compose

## Install 
Create and set the Docker machine
```
$ docker-machine create concrete5
$ docker-machine env concrete5
$ eval $(docker-machine env concrete5)
```
Adjust .env file
```
$ vi .env
```
Install composer deps
```
$ cd site
$ composer install
```
Build and run the containers

```
$ cd ../
$ docker-compose up -d --build
```

Get the IP of the Docker machine
```
$ docker-machine ip concrete5
```
Go to the IP in a browser and install. Make sure to set MYSQL credentials to the environment variables that you set before.
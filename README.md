# Docker skeleton with Postgres DB

This repository contains a basic Docker Compose structure to start your new Symfony ^5.x project. It has a single container with a PHP 8.0.10 interpreter (you can change the version under `docker/Dockerfile`) and some useful tools like:
- Composer: to install dependencies in your Symfony project
- A basic XDEBUG 3 configuration (you can add or remove configuration under `docker/xdebug.ini`)


## Installation
- `make build` to build the project and install dependencies
- `make start` to spin up the application container
- `make ssh-be` to access the of the application container's bash

(check other targets in `Makefile`)

Now you can run `symfony` commands to create a new project and so on. (See https://symfony.com/download for more info)

Note: if you get a GIT error during the creation of a new project just set your GITHUB username and email with:
```
git config --global user.name "[your name]"
git config --global user.email "[your email]"
```
or just use the `--no-git` flag (e.g: `symfony new --dir=my-project --no-git`)
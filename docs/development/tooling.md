# Tooling documentation

The following is a list of technologies and tools used in components, sites and projects developed under the OpenEuropa Initiative.

## Table of Contents

- [Development environment](#development-environment)
  - [System-level packages](#system-level-packages)
  - [PHP](#php)
  - [Composer](#composer)
  - [Git](#git)
  - [Drush](#drush)
  - [Robo](#robo)
  - [Node.js](#node\.js)
- [Validation and testing tools](#validation-and-testing-tools)
  - [Behat](#behat)
  - [PHPUnit](#phpunit)
  - [GrumPhp](#grumphp)
- [CI/CD solutions](#ci\/cd-solutions)  
- [Docker](#docker)
  - [Supported Docker images](#supported-docker-images)
  - [Using Docker Compose](#using-docker-compose)
  - [Using Docker on macOS](#using-docker-on-macos)

### Development environment

OpenEuropa does not impose a development environment as long as the following software packages are used. Nevertheless, all system requirements for each component are containerized using Docker.

#### System-level packages

| Tool | Required | Purpose |
|-|-|-|
| [PHP](#php) | Yes | Required by Composer, Drush, TaskRunner, etc. |
| [Composer](#composer) | Yes | Package manager for PHP. |
| [Git](#git) | Yes | Version control system. |
| [Drush](#drush) | Yes | CLI integration with Drupal. |
| [Robo](#robo) | Yes | Required by OpenEuropa task runner. |
| [Node.js](#npm) | No | Required to develop OpenEuropa theme. |

#### PHP

[PHP](http://php.net/manual/en/install.php) is required by various tools, including Composer, Drush, Robo, and Drupal itself. Please ensure that:

* OpenEuropa components require usage of PHP 7.1+. You can check your existing version by executing `php -v`.

#### Composer

[Composer](https://getcomposer.org/) is used to manage dependencies of PHP projects. It has natural integration with Drupal.org.
All projects developed under OpenEuropa initiative require to use it.
All dependencies specific for given component are defined in its composer.json file.

#### Git

[Git](https://git-scm.com/) is the distributed version control system used as a foundation of the OpenEuropa ecosystem. Components created by OpenEuropa teams are stored in separated repositories hosted on Github.

#### Drush

[Drush](http://www.drush.org/en/master/) is a command line shell and Unix scripting interface for Drupal. Drush is used to interact with Drupal websites through the command line.

#### Robo

[Robo](https://robo.li) is a modern and simple PHP task runner inspired by Gulp and Rake aimed to automate common tasks. It is the main dependency of OpenEuropa [Task Runner](https://github.com/openeuropa/task-runner) project.

#### Node.js

[Node.js (>= 8)](https://nodejs.org/en) is required for the development of OpenEuropa theme. The same development practices described in OpenEuropa theme are recommended also for the development of custom themes.
All required development dependencies are defined in the package.json file.

### Validation and testing tools

| Tool                       |
|----------------------------|
| [Behat](#behat)            |
| [PHPUnit](#phpunit)        |
| [GrumPhp](#grumphp)        |

#### Behat

[Behat](http://behat.org/) is a php framework for autotesting business expectations. It shall be used to develop automated tests using Gherkin scenarios in order to cover business functionalities.

#### PHPUnit

[PHPUnit](https://phpunit.de/) is used by OpenEuropa components to perform unit testing against developed code. PHPUnit is broadly adopted by Drupal community. More information about its usage can be found [here](https://www.drupal.org/docs/8/phpunit).

#### GrumPhp

[GrumpPhp](https://github.com/phpro/grumphp) is used as the dependency in [OpenEuropa Code Review component](https://github.com/openeuropa/code-review) to enforce that PHP coding standards are correctly applied to newly developed code.

### CI/CD solutions

| Tool                       |
|----------------------------|
| [Drone](#drone)            |

#### Drone

Drone is the recommended CI/CD solution for OpenEuropa Initiative. More information about drone can be found [here](docs/development/third-party/drone.md).

### Docker

In order to setup and isolate individual components of the overall OpenEuropa solution, components need to be able to be containerised. Moreover, components should provide a standard solution for a final user to interact with them when used in containers.

Therefore maintainers decided to use Docker technology orchestrated by the usage of docker-compose. In case of any specific information related to the usage and configuration of containers for custom or different purposes, you can find additional documentation at the component repository.

Docker is a platform for developers and sysadmins to develop, deploy, and run applications with containers.

#### Supported Docker images

Containers used in OpenEuropa Initiative projects are based on images crafted by the FPFIS DevOps team. Information about supported images and their configuration can be find under following link [Docker images](https://docs.fpfis.eu/docker-images/).

#### Using Docker Compose

Projects which are delivered under the OpenEuropa Initiative offers a set of containers to mimic software packages used on the IT infrastructure and provide an easy way of setting up an environment to work. If you want to run the containerised environment in order to work with a given component, project or site, you can follow these steps to set up it using Docker Compose.

Requirements:

- [Docker](https://www.docker.com/get-docker)
- [Docker-compose](https://docs.docker.com/compose)

Run:

```bash
docker-compose up -d
```

This will set up and run the environment. After spawning, please follow the set of commands specified in the documentation of a given component, site or a project.
Usually the next step is to execute Composer script to download and set up dependencies.

```bash
docker-compose exec web composer install
```

In order to tweak settings or adjust configuration of a specific container, please edit the `docker-compose.yml` file accordingly to your current needs.

#### Using Docker on macOS

In order to maximise the performance of using Docker on macOS, we strongly advise using at least version 18.03.1 of Docker which supports native NFS integration. You can find a very comprehensive article about this topic under following link [Set Up Docker For Mac with Native NFS](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc).

What is required can be defined in two steps.

First is to run the bash script in order to configure Docker native NFS support.
You can find the source of a script in the article or by using this link [setup_native_nfs_docker_osx.sh](https://gist.githubusercontent.com/seanhandley/7dad300420e5f8f02e7243b7651c6657/raw/fdd77fe66cf9ce893fa0175d735cbede2bb065e4/setup_native_nfs_docker_osx.sh).

Next, you must include an additional volume definition inside the `docker-compose.override.yml` file. OpenEuropa components ship with the volume definition in their `docker-compose.yml` file, commented out. But you can also find the example of how to do so below. 

In the second part keyed by `volumes`, the volume `nfsmount` is defined and configured to use NFS native support. Then you can reference the defined volume as a storage of a container.

In the example below, the `nfsmount` volume is used as a storage for the `web` container and mount to the `var/www/html` directory inside the container. From the local machine perspective it mounts the main directory where the `docker-compose.yml` file is located into the directory configured in a give container (`/var/www/html` in this particular case).

```yml
# Example of the docker-compose.yml file with the additional volume definition.

version: '2'
services:
  web:
    image: fpfis/httpd-php-dev:5.6
    working_dir: /var/www/html
    environment:
      - DOCUMENT_ROOT=/var/www/html
    volumes:
      - nfsmount:/var/www/html
    ports:
      - 8080:8080

volumes:
  nfsmount:
    driver: local
    driver_opts:
      type: nfs
      o: addr=host.docker.internal,rw,nolock,hard,nointr,nfsvers=3
      device: ":${PWD}/"
```

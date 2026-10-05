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
  - [Node.js](#nodejs)
- [Validation and testing tools](#validation-and-testing-tools)
  - [PHPUnit](#phpunit)
  - [GrumPHP](#grumphp)
  - [Behat](#behat)
- [CI/CD solutions](#cicd-solutions)
- [Docker](#docker)
  - [Supported Docker images](#supported-docker-images)
  - [Using Docker Compose](#using-docker-compose)

### Development environment

OpenEuropa does not impose a development environment as long as the following software packages are used. Nevertheless, all system requirements for each component are containerized using Docker.

#### System-level packages

| Tool | Required | Purpose |
|-|-|-|
| [PHP](#php) | Yes | Required by Composer, Drush, Task Runner, etc. |
| [Composer](#composer) | Yes | Package manager for PHP. |
| [Git](#git) | Yes | Version control system. |
| [Drush](#drush) | Yes | CLI integration with Drupal. |
| [Robo](#robo) | Yes | Required by OpenEuropa Task Runner. |
| [Node.js](#nodejs) | No | Required to develop OpenEuropa themes. |

#### PHP

[PHP](https://www.php.net/manual/en/install.php) is required by various tools, including Composer, Drush, Robo, and Drupal itself.
OpenEuropa components require PHP 8.1 or newer; check the `composer.json` of each component for its exact requirement. You can check your existing version by executing `php -v`.

#### Composer

[Composer](https://getcomposer.org/) is used to manage dependencies of PHP projects. It has natural integration with Drupal.org.
All projects developed under OpenEuropa initiative require to use it.
All dependencies specific for given component are defined in its composer.json file.

#### Git

[Git](https://git-scm.com/) is the distributed version control system used as a foundation of the OpenEuropa ecosystem. Components created by OpenEuropa teams are stored in separated repositories hosted on GitHub.

#### Drush

[Drush](https://www.drush.org/) is a command line shell and Unix scripting interface for Drupal. Drush is used to interact with Drupal websites through the command line.

#### Robo

[Robo](https://robo.li) is a modern and simple PHP task runner inspired by Gulp and Rake aimed to automate common tasks. It is the main dependency of OpenEuropa [Task Runner](https://github.com/openeuropa/task-runner) project.

#### Node.js

[Node.js](https://nodejs.org/en) is required for the development of OpenEuropa themes. Check the `engines` section of the theme's `package.json` for the required Node.js and package manager versions. The same development practices described in OpenEuropa theme are recommended also for the development of custom themes.
All required development dependencies are defined in the package.json file.

### Validation and testing tools

| Tool                       |
|----------------------------|
| [PHPUnit](#phpunit)        |
| [GrumPHP](#grumphp)        |
| [Behat](#behat)            |

#### PHPUnit

[PHPUnit](https://phpunit.de/) is used by OpenEuropa components to test the developed code. PHPUnit is broadly adopted by Drupal community. More information about its usage can be found [here](https://www.drupal.org/docs/develop/automated-testing/phpunit-in-drupal).

#### GrumPHP

[GrumPHP](https://github.com/phpro/grumphp) is used by the [OpenEuropa Code Review Drupal](https://github.com/openeuropa/code-review-drupal) and [OpenEuropa Code Review Library](https://github.com/openeuropa/code-review-library) components to enforce that coding standards are correctly applied to newly developed code.

#### Behat

[Behat](https://docs.behat.org/) is being phased out. Existing scenarios are still supported by the CI pipelines, but new tests should be written with [PHPUnit](#phpunit). See [Testing Drupal components](testing.md).

### CI/CD solutions

OpenEuropa components use GitHub Actions for continuous integration. More information can be found in [CI Deployment Workflow](ci-deployment-workflow.md).

### Docker

In order to setup and isolate individual components of the overall OpenEuropa solution, components need to be able to be containerised. Moreover, components should provide a standard solution for a final user to interact with them when used in containers.

Therefore maintainers decided to use Docker technology orchestrated by Docker Compose. In case of any specific information related to the usage and configuration of containers for custom or different purposes, you can find additional documentation at the component repository.

#### Supported Docker images

Containers used in OpenEuropa Initiative projects are based on images crafted by the FPFIS DevOps team, such as [fpfis/httpd-php](https://hub.docker.com/r/fpfis/httpd-php). Check the `docker-compose.yml` file of each component for the images it uses.

#### Using Docker Compose

Projects which are delivered under the OpenEuropa Initiative offer a set of containers to mimic software packages used on the IT infrastructure and provide an easy way of setting up an environment to work. If you want to run the containerised environment in order to work with a given component, project or site, you can follow these steps to set it up using [Docker Compose](https://docs.docker.com/compose/).

Run:

```bash
docker compose up -d
```

This will set up and run the environment. After spawning, please follow the set of commands specified in the documentation of a given component, site or a project.
Usually the next step is to execute Composer to download and set up dependencies.

```bash
docker compose exec web composer install
```

In order to tweak settings or adjust configuration of a specific container, create a `docker-compose.override.yml` file rather than editing `docker-compose.yml`.

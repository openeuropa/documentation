The following is a list of technologies and tools used in OpenEuropa project.

# Development environment
OpenEuropa does not impose a development environment as long the following software packages are used. Nevertheless, all system requirements for each component are containerized using Docker Compose. 

### System-level packages

| Tool                          | Required | Purpose                                  |
|-------------------------------|----------|------------------------------------------|
| [PHP](#php)                   | Yes      | Required by Composer, Drush, TaskRunner, etc. |
| [Composer](#composer)         | Yes      | Package management.                      |
| [Git](#git)                   | Yes      | Version control.                         |
| [Drush](#drush)               | Yes      | CLI integration with Drupal.             |
| [Robo](#robo)               | Yes      | Required by OpenEuropa task runner.             |
| [Docker/Docker-Compose](#dockercompose)    | No       | Used to setup development environments for the different components    |
| [Node.js](#npm)               | No       | Required to develop OpenEuropa theme     |

### <a name="php">PHP</a>

[PHP](http://php.net/manual/en/install.php) is required by various tools, including Composer, Drush, Robo, and Drupal itself. Please ensure that:

* OpenEuropa componentes require usage of PHP 7.1+. You can check your existing version by executing `php -v`

### <a name="composer">Composer</a>

[Composer](https://getcomposer.org/) is used to manage project level dependencies for PHP projects. It has natural integration with Drupal.org.
Any project in OpenEuropa initiative is required to use it.
All PHP project dependencies are defined by each component in its composer.json

### <a name="git">Git</a>

[Git](https://git-scm.com/) is the distributed version control system in use by OpenEuropa iniative. Components create by OpenEuropa teams are controlled in individual repositoroes in Github.

### <a name="drush">Drush</a>

[Drush](http://www.drush.org/en/master/) is a command line shell and Unix scripting interface for Drupal. 
Drush is used to interface with drupal web sites through the command line.

### <a name="robo">Robo</a>

[Robo](https://robo.li) is a modern and simple PHP task runner inspired by Gulp and Rake aimed to automate common tasks 
used by OpenEuropa [Task Runner](https://github.com/openeuropa/task-runner)

### <a name="dockercompose">Docker Compose</a>

[Docker compose)](https://docs.docker.com/compose) can be used to quickly setup a development environment for the different components assuring all the required dependencies are present.

### <a name="npm">Node.js</a>

[Node.js (>= 8)](https://nodejs.org/en) is required for the development of OpenEuropa theme. The same development pratices described in OpenEuropa theme are recommended also for the development of custom themes.
All Node.js development dependencies are required in the repository package.json

## Validation & testing tools

| Tool                       |
|----------------------------|
| [Behat](#behat)            |
| [PHPUnit](#phpunit)        |
| [GrumPhp](#grumphp) |

### <a name="behat">Behat</a>

[Behat)](http://behat.org/) should be used to develop automatic functional tests that guarantee business funcionality.

### <a name="PHPUnit">PHPUnit</a>

[PHPUnit](https://phpunit.de/) is used by OpenEuropa components to perform unit testing against developed code. PHPUnit is broadly adapted by Drupal community and more information about its usage can be found [here](https://www.drupal.org/docs/8/phpunit)

### <a name="grumPhp">GrumPhp</a>

[GrumpPhp](https://github.com/phpro/grumphp) is used in [OpenEuropa Code Review component](https://github.com/openeuropa/code-review) to guarantee PHP coding standards are correctly applied to new developed code.


## CI/CD solutions

| Tool                       |
|----------------------------|
| [Drone](#drone)            |

### <a name="drone">Drone</a>
Drone is the recommended CI/CD solution for OpenEuropa Initiative. More information about drone can be found [here](docs/development/third-party/drone.md)


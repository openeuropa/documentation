The following is a list of technologies and tools used in OpenEuropa project.

# Development environment
OpenEuropa does not impose a development environment as long as the following software packages are used. Nevertheless, all system requirements for each component are containerized using Docker. 

### System-level packages

| Tool                          | Required | Purpose                                  |
|-------------------------------|----------|------------------------------------------|
| [PHP](#php) | Yes | Required by Composer, Drush, TaskRunner, etc. |
| [Composer](#composer) | Yes | Package manager for PHP. |
| [Git](#git) | Yes | Version control system. |
| [Drush](#drush) | Yes | CLI integration with Drupal. |
| [Robo](#robo) | Yes | Required by OpenEuropa task runner. |
| [Docker/Docker-Compose](#dockercompose) | No | Used to setup development environments for the different components. |
| [Node.js](#npm) | No | Required to develop OpenEuropa theme. |

### <a name="php">PHP</a>

[PHP](http://php.net/manual/en/install.php) is required by various tools, including Composer, Drush, Robo, and Drupal itself. Please ensure that:

* OpenEuropa components require usage of PHP 7.1+. You can check your existing version by executing `php -v`.

### <a name="composer">Composer</a>

[Composer](https://getcomposer.org/) is used to manage dependencies of PHP projects. It has natural integration with Drupal.org.
All projects developed under OpenEuropa initiative require to use it.
All dependencies specific for given component are defined in its composer.json file.

### <a name="git">Git</a>

[Git](https://git-scm.com/) is the distributed version control system used as a foundation of the OpenEuropa ecosystem. Components created by OpenEuropa teams are stored in separated repositories hosted on Github.

### <a name="drush">Drush</a>

[Drush](http://www.drush.org/en/master/) is a command line shell and Unix scripting interface for Drupal. Drush is used to interact with Drupal websites through the command line.

### <a name="robo">Robo</a>

[Robo](https://robo.li) is a modern and simple PHP task runner inspired by Gulp and Rake aimed to automate common tasks. It is the main dependency of OpenEuropa [Task Runner](https://github.com/openeuropa/task-runner) project.

### <a name="dockercompose">Docker Compose</a>

[Docker compose](https://docs.docker.com/compose) facilitates the use of Docker solutions in order to set up quickly a development environment for the different components ensuring that all technical requirements are met and dependencies are present.

### <a name="npm">Node.js</a>

[Node.js (>= 8)](https://nodejs.org/en) is required for the development of OpenEuropa theme. The same development practices described in OpenEuropa theme are recommended also for the development of custom themes.
All required development dependencies are defined in the package.json file.

## Validation & testing tools

| Tool                       |
|----------------------------|
| [Behat](#behat)            |
| [PHPUnit](#phpunit)        |
| [GrumPhp](#grumphp)        |

### <a name="behat">Behat</a>

[Behat](http://behat.org/) is a php framework for autotesting business expectations. It shall be used to develop automated tests using Gherkin scenarios in order to cover business functionalities.

### <a name="PHPUnit">PHPUnit</a>

[PHPUnit](https://phpunit.de/) is used by OpenEuropa components to perform unit testing against developed code. PHPUnit is broadly adopted by Drupal community. More information about its usage can be found [here](https://www.drupal.org/docs/8/phpunit).

### <a name="grumPhp">GrumPhp</a>

[GrumpPhp](https://github.com/phpro/grumphp) is used as the dependency in [OpenEuropa Code Review component](https://github.com/openeuropa/code-review) to enforce that PHP coding standards are correctly applied to newly developed code.

## CI/CD solutions

| Tool                       |
|----------------------------|
| [Drone](#drone)            |

### <a name="drone">Drone</a>
Drone is the recommended CI/CD solution for OpenEuropa Initiative. More information about drone can be found [here](docs/development/third-party/drone.md).

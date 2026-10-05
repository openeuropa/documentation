# Repository scaffolding

Repositories follow a common structure that allows for a fast and easy development setup.

There is no maintained repository template. When creating a new component, start from the setup files of an existing, actively maintained component such as [OpenEuropa Content](https://github.com/openeuropa/oe_content):

- `composer.json`;
- `docker-compose.yml` for the [development environment](../development/tooling.md#docker);
- `runner.yml.dist` for the [Task Runner](https://github.com/openeuropa/task-runner);
- `grumphp.yml.dist` for the [coding standards](../development/coding-standards.md) checks;
- `phpunit.xml.dist` for the [tests](../development/testing.md);
- `.github/workflows/ci.yml` for the [CI pipeline](../development/ci-deployment-workflow.md).

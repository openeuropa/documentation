# CI Deployment Workflow

OpenEuropa components use [GitHub Actions](https://docs.github.com/en/actions) for continuous integration. Pipelines run automatically on pull requests and on pushes to the default branch.

The pipeline definitions are shared: each component has a small `.github/workflows/ci.yml` file that calls a reusable workflow from the [OpenEuropa GitHub CI repository](https://github.com/openeuropa/github-ci):

- `drupal-ci.yml` for Drupal modules and themes;
- `php-library-ci.yml` for PHP libraries.

```yaml
name: ci
on:
  pull_request:
    types: [opened, synchronize]
  push:
    branches:
      - 1.x

jobs:
  automated-tests:
    uses: openeuropa/github-ci/.github/workflows/drupal-ci.yml@main
```

The Drupal workflow starts the component's `docker-compose.yml` stack, runs GrumPHP and PHPUnit, and repeats this for every PHP and Drupal core version in its test matrix. Inputs such as `php_versions`, `core_versions`, `run_phpunit_batches` and `run_behat` can be set in the component's `ci.yml`; see the reusable workflow for their defaults.

# Automated testing

OpenEuropa requires automated tests to be written for every new feature or
bugfix to ensure that the functionality will keep working as expected in the
future.

## Acceptance criteria

* Pull requests without sufficient test coverage will not be accepted.
* As a general rule any non-trivial code should be covered with tests. Trivial
  code that does not contain any business logic (such as getters and setters,
  object constructors, factory methods, ...) does not require tests. However,
  any code that is non-trivial (e.g. containing switches, loops, arithmetic
  operations or any other business logic) should be fully covered by tests.
* Whether or not a piece of code is missing necessary coverage is at the
  discretion of the QA engineers. Any request for additional test coverage
  during code review needs to be honoured or the pull request will not be
  accepted.
* For a pull request to be accepted, both the previously existing and the newly
  added tests should be passing.
* Existing test code should not be modified unless this is backed up by a change
  request originating from project stakeholders.

## Types of tests

OpenEuropa is phasing out [Behat][1]. New tests are written with [PHPUnit][2],
or with the standard unit testing framework of the programming language in which
the component is developed. Do not add new Behat scenarios. Existing scenarios
must keep passing until they are migrated to PHPUnit.

Test both the business requirements and the code that implements them:

* User-facing behaviour described in a user story is covered by tests that act
  as the user would, for example functional tests in Drupal components.
* Non-trivial code, and code intended to be reused, is covered by unit tests,
  since business requirements may change and leave parts of the code untested.

See [Testing Drupal components](testing.md) for how this applies to Drupal.

## Running tests

In order to ensure that the project fully benefits from the advantages of
automated testing we require the following:

* Every project and component in the OpenEuropa space should use a Continuous
  Integration service to automatically test every PR before they get accepted.
  The OpenEuropa team provides this service. For more information see [CI
  Deployment Workflow](ci-deployment-workflow.md).
* Every component is required to add a section to the main README file that
  explains how to run the test suite on a local development environment. This
  will ensure that any contributor will have this important information readily
  available.

[1]: https://docs.behat.org/
[2]: https://phpunit.de/

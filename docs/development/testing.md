# Testing Drupal components

This document contains information specific to testing Drupal based components.
More general information about our testing policy can be found in the
[Automated testing](automated-testing.md) section.

## Choosing the right test framework

Drupal components are tested with the PHPUnit based frameworks that ship with
Drupal core, described in [Types of tests][1].

OpenEuropa is phasing out Behat. Do not add new Behat scenarios; write PHPUnit
tests instead. Existing Behat scenarios must keep passing until they are
migrated.

Guidelines:

* Provide tests for the public API: public methods as described in interfaces.
* Prefer low level testing frameworks over higher level ones. Choose the lowest
  level that covers your needs:
  * `UnitTestCase` is preferred.
  * Use `KernelTestBase` if you need to test the interaction of your code with
    the Drupal API.
  * Use `BrowserTestBase` (functional tests) to test end user behaviour, such
    as the business requirements described in a user story.
  * Use `WebDriverTestBase` (functional JavaScript tests) only when the
    behaviour depends on JavaScript.
* Functional tests should be executed as the user described in the
  requirement, for example as an anonymous user, so that access checks and
  caching are covered.
* [OpenEuropa Testing Utilities][2] provides helpers shared by the components,
  such as a trait that caches the site installation to speed up functional
  tests.

## Writing tests for bug fixes

* Tickets that are marked as bug fixes might affect end user behaviour. If a
  fix changes behaviour that was described in the business requirements, this
  should be discussed with the business stakeholders and approved by them.
* When writing a test for a bug fix it is highly recommended to write and
  commit the test first, so it can be demonstrated that the test correctly fails
  when the bug is present, and passes when the bug is fixed.

## Running tests

* Every Drupal component should have a section in the README explaining how to
  run the tests on a local development environment.
* Provide the necessary configuration files (like `phpunit.xml.dist`) in the
  root of the project to make execution of tests as trivial as possible.
* Ensure that the tests run on our Continuous Integration environment by
  supplying a `.github/workflows/ci.yml` file. See
  [CI Deployment Workflow](ci-deployment-workflow.md).

[1]: https://www.drupal.org/docs/develop/automated-testing/types-of-tests
[2]: https://github.com/openeuropa/oe_testing_utils

# Testing Drupal components

This document contains information specific to testing Drupal based components.
More general information about our testing policy can be found in the
[Automated testing](../../../../docs/automated-testing.md) section.

## Choosing the right test framework

In addition to the built-in testing frameworks that ship with Drupal core,
OpenEuropa also uses Behat to describe business requirements. This section
details which test framework to use under which circumstances.

### Behat

Whenever a PR intends to change end user behaviour it is required to describe
the expected user behaviour in a Behat scenario. In practice this means:

* Every user story is accompanied by a Behat scenario. This scenario will be
  provided to the project stakeholders for acceptance testing.
* The target audience for these scenarios are the project stakeholders. The
  Behat scenarios prove to project stakeholders that the project fulfills all
  business requirements.
* Every Behat test scenario is written in domain specific business language.
  The scenarios should avoid the use of technical terms, machine names or
  references to underlying technology which might not be understood by
  non-technical stakeholders.
* Behat tests should only be used to describe expected user behaviour as
  specified by project stakeholders. It should *not* be used to test code. Any
  code written that does not directly affect the expected end user behaviour
  should be covered by unit tests instead. At no point the business should see
  a Behat scenario that describes a behaviour that was not directly requested
  by them.
* For many user stories the Behat scenario will be sufficient to cover the full
  extent of the code that was written. However, business requirements are known
  to change which might leave critical code paths untested. For this reason it
  is recommended that any non-trivial code is covered by unit tests in addition
  to Behat scenarios.

### Unit tests

Pull requests that are not part of user stories should be covered by unit tests
rather than Behat scenarios. It is also recommended to provide unit tests for
any code that is non-trivial or is intended to be reused (like services or
plugins).

Guidelines for writing unit tests:

* The different test frameworks are described in [Types of tests in Drupal
  8][1]. 
* Provide tests for the public API: public methods as described in interfaces.
* Prefer low level testing frameworks over higher level ones. Choose the lowest
  level that covers your needs. `UnitTestCase` is preferred. Only use 
  `KernelTestBase` if you actually need to test the interaction of your code
  with the Drupal API.
* Functional tests (`BrowserTestBase`) should be rarely needed since this tests
  end user behaviour. If any end user behaviour needs to be tested, please
  consult the business stakeholders if this behaviour can be captured in actual
  business requirements instead. This would allow us to use Behat scenarios 
  which are prefered over functional tests in PHPUnit.
* Javascript code is most commonly written in function of business requirements
  that directly affect end user behaviour. Work with business stakeholders to
  see if this can be put into a user story, and a corresponding Behat scenario.
  Only in the rare case that JS code is not correlating with requested end user
  behaviour `JavascriptTestBase` should be used.

## Writing tests for bug fixes

* Tickets that are marked as bug fixes might affect end user behaviour. In many
  cases a bug fix might be caused by a previously undescribed user behaviour, or
  insufficient coverage of edge cases in Behat scenarios. If a ticket is marked
  as a bugfix but might necessitate changes in Behat scenarios this should be
  discussed with the business stakeholders and approved by them.
* Other types of bugs might not directly affect the expected end user
  behaviour. Examples are error messages, crashes, cache invalidation problems
  etc. These can often be fixed without requiring changes to the business
  requirements, and hence no changes to Behat scenarios are required.
* When writing a test for a bug fix it is highly recommended to write and
  commit the test first, so it can be demonstrated that the test correctly fails
  when the bug is present, and passes when the bug is fixed.

## Running tests

* Every Drupal component should have a section in the README explaining how to
  run the tests on a local development environment.
* Provide the necessary configuration files (like `phpunit.xml.dist` and
  `behat.yml.dist`) in the root of the project to make execution of tests as
  trivial as possible.
* Ensure that the tests can run on our Continuous Integration environments by
  supplying a `.drone.yml` file.

[1]: https://www.drupal.org/docs/8/testing/types-of-tests-in-drupal-8 

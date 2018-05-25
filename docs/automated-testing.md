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

### User stories

OpenEuropa practices [Behaviour Driven Development][1] to facilitate effective
communication between business and development teams.

User stories, or business requirements in general, should be accompanied by a
test scenario that is written in non-technical domain specific language. This
scenario should be verified by the business during user acceptance testing.
After the story is accepted this scenario can then be used to perform automated
tests to ensure that the business requirements work as designed, and keep
working for the entire lifetime of the project.

Every OpenEuropa component should write their test scenarios in [Gherkin][2]
and use a BDD framework appropriate for their programming language to execute
and verify the scenarios. For example, in PHP based code we can use [Behat][3].

For many user stories having a BDD user scenario can be sufficient to fully
test all code that has been written to fulfill the user story. However since it
might happen that business requirements change in the future this may cause
existing scenarios to be rewritten, which might leave parts of the code
untested. For this reason it is highly recommended to provide unit tests in
addition to BDD scenarios, especially for business critical components and code
that is intended to be reused.

Note that according to BDD principles the user scenarios are solely intended
for describing expected user behaviour. They should not be used to provide test
coverage for any code that does not directly correspond to a user story that
was provided by the business. The main audience for these user scenarios are
the product owner and business stakeholders who can inspect the scenarios at
any time to verify that the business value is being realized by the project.
Any change or addition to the user scenarios can be seen as a change to the
business requirements, and should be approved by business stakeholders.

### Unit tests

Any pull requests that do not result from user stories should be covered by
unit tests rather than BDD user scenarios. Use the appropriate unit testing
frameworks that are available for the programming language in which your
component is developed.

## Running tests

In order to ensure that the project fully benefits from the advantages of
automated testing we require the following:

* Every project and component in the OpenEuropa space should use a Continuous
  Integration service to automatically test every PR before they get accepted.
  The OpenEuropa team provides this service. For more information see [CI
  Deployment Workflow](docs/development/ci-deployment-workflow.md).
* Every component is required to add a section to the main README file that
  explains how to run the test suite on a local development environment. This
  will ensure that any contributor will have this important information readily
  available.

[1]: https://en.wikipedia.org/wiki/Behavior-driven_development
[2]: https://github.com/cucumber/cucumber/wiki/Gherkin
[3]: http://behat.org/

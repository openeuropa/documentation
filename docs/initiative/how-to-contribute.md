# Contributing to OpenEuropa

The following is a set of guidelines for contributing to OpenEuropa and its components, which are hosted in the
[OpenEuropa project](https://github.com/openeuropa) on GitHub. These are mostly guidelines, not rules.
Use your best judgment, and feel free to propose changes to this document in a pull request.

**Table of contents**

* [Code of conduct](#code-of-conduct)
* [Before getting started](#before-getting-started)
* [How can I contribute?](#how-can-i-contribute)
  * [Reporting bugs](#reporting-bugs)
  * [Feature requests](#feature-requests)
  * [Pull requests](#pull-requests)
* [Style guide](#style-guide)
  * [Git commit messages](#git-commit-messages)
  * [Code styling](#code-styling)

## Code of conduct

This project and everyone participating in it is governed by the [OpenEuropa Code of Conduct](code-of-conduct.md).
By participating, you are expected to uphold this code. Please report unacceptable behaviour to [digit-nexteuropa-core-team@ec.europa.eu](mailto:digit-nexteuropa-core-team@ec.europa.eu).

## Before getting started

OpenEuropa is an open source project made up of several components. Before you report anything please make
sure you are using the correct repository for the component you are referring to.

A comprehensive list of components built and maintained by the OpenEuropa team is available [here](../openeuropa-components.md).

## How can I contribute?

### Reporting bugs

This section guides you through submitting a bug report for any OpenEuropa component. Following these guidelines helps
everyone involved to understand your report and react efficiently.

Before creating bug reports, please check [this checklist](#before-submitting-a-bug-report) as you might find out that
you don't actually need to create one. When you are creating a bug report, please [include as many details as possible](#how-do-i-submit-a-good-bug-report)
and use [the required template](../templates/issue-template.md), this will allows us to resolve issues faster.

#### Before submitting a bug report

* Determine [which repository the problem should be reported in](#before-getting-started).
* Make sure the issue is really a bug and not an intended behaviour by reading the component's documentation.
* Check if you can reproduce the problem in the latest version of the related component.
* Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3Aopeneuropa) to see if the problem has
  already been reported. If it has and the issue is still open, please add a comment to the existing issue instead of
  opening a new one.

#### How do I submit a (good) bug report?

Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues). After you've determined [which repository](#before-getting-started)
your bug is related to, create an issue on that repository and provide the following information by filling in
[the issue template](../templates/issue-template.md).

Explain the problem and include additional details to help maintainers reproduce the issue:

* Use a clear and descriptive title that describes the problem.
* Describe the exact steps necessary to reproduce the problem with as many details as possible.
* Describe the behaviour you observed after following the steps and point out exactly what the problem is with that
  behaviour.
* Explain what the expected behaviour is and why.
* When applicable include screenshots or any other supporting material.

Provide more context by answering these questions:

* Did the problem start happening recently (e.g. after updating to a newer version of the component) or was it always a
  problem?
* If the problem started happening recently, can you reproduce the problem in an older version of the component?
* What's the most recent version in which the problem does not occur?
* Can you reliably reproduce the issue? If not, provide details about how often the problem happens and under which
  circumstances.

Include details about your configuration and environment:

* Which version of the component are you using?
* What's the name and version of the browser you are using?
* Which other components or modules do you have installed?

### Feature requests

This section guides you through submitting a feature request for OpenEuropa, such as completely new features or
improvements to existing functionality.

Before creating a feature request, please check [this checklist](#before-submitting-a-feature-request) as you might find
out that you don't need to create one. When you are creating a feature request, please
[include as many details as possible](#how-do-i-submit-a-good-feature-request).

Fill in [the issue template](../templates/issue-template.md), including the steps that you imagine you would take if the feature
you're requesting existed.

#### Before submitting a feature request

* Check if there's already [a component](../openeuropa-components.md) which provides that enhancement.
* Check the project roadmap to understand if the feature is already being planned for future releases associated dates.
* Determine [which repository the feature should be suggested in](#before-getting-started).
* Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3Aopeneuropa) to see if the feature has
  already been suggested. If it has, add a comment to the existing issue instead of opening a new one.

#### How do I submit a (good) feature request?

Feature requests are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined
[which repository](#before-getting-started) your feature suggestion is related to, create an issue on that repository
and provide the following information:

* Use a clear and descriptive title for the issue to identify the suggestion.
* Provide a step-by-step description of the suggested enhancement in as many details as possible.
* Describe the current behaviour and explain which behaviour you expected to see instead and why.
* Include screenshots which will help demonstrate the feature you would like to include.
* Explain why this enhancement would be useful to the users of the component and isn't something that can or should be
  implemented as a custom component.

### Pull requests

* Fill in the provided template. You can see a sample [here](../templates/pull-request-template.md).
* Make sure to include (if not available yet) and run the [Code Review component](https://github.com/openeuropa/code-review)
  before submitting the pull request.
* End all files with a newline.

## Style guide

### Git commit messages

* If the commit refers to an issue or a ticket, start the comment with the issue or ticket number,
  then add a colon and a space ("#1234: " or "OPENEUROPA-1234: ").
* Prefer the present tense ("Add feature" not "Added feature").
* Prefer the imperative mood ("Move element to..." not "Moves element to...").
* Limit the first line to 72 characters or less.
* Do not end the first line with a period.

Example of commit message: "#1234: Implement automatic feature generator".

### Code styling

OpenEuropa provides a specific component to enforce a series of code styling rules. Please make sure that the
[Code Review component](https://github.com/openeuropa/code-review) is included in the component you are working with and
that the results are all green before committing anything.

# Contributing to OpenEuropa

The following is a set of guidelines for contributing to OpenEuropa and its components, which are hosted in the [OpenEuropa project](https://github.com/openeuropa) GitHub. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

#### Table Of Contents

[Code of Conduct](#code-of-conduct)

[Before getting started](#before-getting-started)

[How Can I Contribute?](#how-can-i-contribute)
  * [Reporting Bugs](#reporting-bugs)
  * [Feature requests](#feature-requests)
  * [Pull Requests](#pull-requests)

[Styleguides](#styleguides)
  * [Git Commit Messages](#git-commit-messages)
  * [Code styling](#code-styling)

## Code of Conduct

This project and everyone participating in it is governed by the [OpenEuropa Code of Conduct](code-of-conduct.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [TODO:add mail](mailto:TODO).

## Before getting started

OpenEuropa is an open source project made up of several different components. Before you report anything please make sure you are using the correct repository for the component you are referring to. 

The following is a comprehensive list of components built and maintained by the OpenEuropa team: [OpenEuropa component list](openeuropa-components.md)

## How Can I Contribute?

### Reporting Bugs

This section guides you through submitting a bug report for any OpenEuropa component. Following these guidelines helps everyone involved understand your report and react accordingly.

Before creating bug reports, please check [this list](#before-submitting-a-bug-report) as you might find out that you don't need to create one. When you are creating a bug report, please [include as many details as possible](#how-do-i-submit-a-good-bug-report) and use [the required template](ISSUE_TEMPLATE.md), this will allows us to resolve issues faster.


#### Before Submitting A Bug Report

* **Determine [which repository the problem should be reported in](#before-getting-started)**.
* **Make sure the issue is really a bug and not an intended behavior** by carefully reading the component's user manual.
* **Check if you can reproduce the problem in the latest version of the affected component.**
* **Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3Aopeneuropa)** to see if the problem has already been reported. If it has **and the issue is still open**, add a comment to the existing issue instead of opening a new one.

#### How Do I Submit A (Good) Bug Report?

Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined [which repository](#before-getting-started) your bug is related to, create an issue on that repository and provide the following information by filling in [the template](issue-template.md).

Explain the problem and include additional details to help maintainers reproduce the problem:

* **Use a clear and descriptive title** for the issue to identify the problem.
* **Describe the exact steps which reproduce the problem** in as many details as possible.
* **Describe the behavior you observed after following the steps** and point out what exactly is the problem with that behavior.
* **Explain which behavior you expected to see instead and why.**
* **Include screenshots** if they help understand the steps or the result.

Provide more context by answering these questions:

* **Did the problem start happening recently** (e.g. after updating to a new version of the component) or was this always a problem?
* If the problem started happening recently, **can you reproduce the problem in an older version of the component?** What's the most recent version in which the problem doesn't happen?
* **Can you reliably reproduce the issue?** If not, provide details about how often the problem happens and under which conditions it normally happens.

Include details about your configuration and environment:

* **Which version of the component are you using?**
* **What's the name and version of the browser you are using**?
* **Which other components or modules do you have installed?**

### Feature requests

This section guides you through submitting a feature request for OpenEuropa, including completely new features and minor improvements to existing functionality.

Before creating a feature request, please check [this list](#before-submitting-a-feature-request) as you might find out that you don't need to create one. When you are creating a feature request, please [include as many details as possible](#how-do-i-submit-a-good-enhancement-suggestion). Fill in [the template](issue-template.md), including the steps that you imagine you would take if the feature you're requesting existed.

#### Before Submitting A Feature Request

* **Check if there's already [a component](openeuropa-components.md) which provides that enhancement.**
* **Determine [which repository the feature should be suggested in](#before-getting-started).**
* **Perform a [cursory search](https://github.com/search?q=+is%3Aissue+user%3Aopeneuropa)** to see if the feature has already been suggested. If it has, add a comment to the existing issue instead of opening a new one.

#### How Do I Submit A (Good) Feature Request?

Feature requests are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined [which repository](#before-getting-starter) your feature suggestion is related to, create an issue on that repository and provide the following information:

* **Use a clear and descriptive title** for the issue to identify the suggestion.
* **Provide a step-by-step description of the suggested enhancement** in as many details as possible.
* **Describe the current behavior** and **explain which behavior you expected to see instead** and why.
* **Include screenshots** which will help demonstrate the feature you would like to include.
* **Explain why this enhancement would be useful** to the users of the component and isn't something that can or should be implemented as a custom component.

### Pull Requests

* Fill in the provided template. You can see a sample [here](pull-request-template.md)
* Make sure include (if not available yet) and run the [Code Review component](https://github.com/openeuropa/code-review) before submitting the pull request.
* End all files with a newline

## Styleguides

### Git Commit Messages

* Start the comment with the ticket number.
* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move element to..." not "Moves element to...")
* Limit the first line to 72 characters or less.

### Code styling

OpenEuropa provides an specific component to enforce a series of code styling rules. Please make sure that the [Code Review component](https://github.com/openeuropa/code-review) is included in the component you are working with and that the results are all green before committing anything.
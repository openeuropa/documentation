# Dependency management

OpenEuropa components often depend on external libraries or Drupal modules. These are included in the component's `composer.json` file but their version
is not locked using a `composer.lock` file. This means that every time the component is installed for development purposes, it will use the latest version
of its dependencies.

In order to ensure that components work with every supported Drupal core version, the [continuous integration pipelines](ci-deployment-workflow.md) install and test them against each
Drupal core version in the test matrix.

Components made for Drupal modules can and very often do include submodules that may have their own dependencies which are not necessarily needed by the parent component as a whole or the other submodules.
In such cases, the dependencies are not declared in the `composer.json` of the main component but are mentioned in the submodule's README file. They are however included in the list of Composer development dependencies
so that they can be loaded and tested during the development of the component.

Dependencies can also be patched using the Composer-based patching plugin. However, if patches are needed for production use (as opposed to patching development dependencies), they should be declared in the component README file.

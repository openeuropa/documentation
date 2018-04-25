# Drupal core experimental module policy

Drupal 8 core introduced the concept of [experimental modules][1].
These are modules that are provided with Drupal core for testing purposes, but that are not yet fully supported.
They offer a wide range of functionalities, from migration management
to site layout management.

Due to the experimental nature of these modules, the OpenEuropa platform
needs to define a set of policies on their use inside OpenEuropa Components.

## Minimum stability required

Currently the experimental modules follow the different stability levels defined by Drupal:
alpha, beta, rc and stable.

In order for OpenEuropa to provide a stable enough set of components, only experimental modules
in **beta state or greater** will be allowed to be used.

This is done because modules in beta state have a very stable API.
Whenever an API change is done, great care is taken to provide a backwards compatibility layer
with deprecated functions that ensure the API remains intact
until developers find the time to update their code to use the new API.
See the official [documentation][2] for more information on the subject.

## Experimental modules in alpha state

Although as a general rule OpenEuropa will not ship with experimental modules in alpha state,
we recognize the potential value that such modules can provide to our customers.

If from a technical or business view the functionality of an alpha experimental module is absolutely required,
a component will be allowed to make use of the required alpha experimental module. 

However, in such cases the components will also use the same label as the experimental module they are using.
This means that a component using an unstable alpha module will also use the alpha label until the related module
changes it.

[1]: https://www.drupal.org/core/experimental
[2]: https://www.drupal.org/core/d8-allowed-changes#beta
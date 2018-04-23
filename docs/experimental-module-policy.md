# Drupal Core Experimental module policy

Drupal 8 core introduced the concept of experimental modules.
These are modules that are provided with Drupal core for testing purposes, but that are not yet fully supported.
They offer a wide range of functionalities, from migration management
to site layout management.

Due to the experimental nature of the modules from the OpenEuropa platform
we need to define a set of policies on their use inside OpenEuropa Components.

## Minimum stability required

Currently the experimental modules follow the different stability levels defined by Drupal:
alpha, beta, rc and stable.

In order for OpenEuropa to provide a stable enough set of components, only experimental modules
in **beta state or greater** will be allowed to be used.

This is done because modules in beta state have a stable API that will only be changed
in very extreme circumstances.

## Experimental modules in alpha state

Although as a general rule OpenEuropa will not ship with experimental modules in alpha state,
we recognize the potential value that such modules can provide to our customers.

If from a technical or business view the functionality of an alpha experimental module is absolutely required,
a component will be allowed to make use of the required alpha experimental module. 

However, in such cases the components will also be labeled as experimental components
and as such will follow the same life cycle of the experimental module they are using. 
This effectively means that an experimental component is subject to be deprecated and removed.


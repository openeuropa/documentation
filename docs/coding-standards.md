# Coding Standards in OpenEuropa

OpenEuropa and all its components are built with public contribution in mind. 
In order for all contributions and components to look and feel familiar
OpenEuropa has agreed on a set of coding standards that all contributors must follow.

Although OpenEuropa does not define any coding standard as such, all the standards it follows
are usually based on well known standards such as [PSR-1][1], [PSR-2][2] and [PSR-4][3].

## How to make your code follow the Coding Standards

In order to make it easier for contributors to create new components or to modify existing ones
the [Code Review][4] component has been created.

This component should be added to the dependency list of any other existing component on OpenEuropa
and it will make sure that all the appropriate standards are followed.
Please refer to the Code Review Readme for more information on usage.

## Coding Standards on Drupal Components

All Drupal based components must follow the already defined [Drupal Coding Standards][5].
This applies to all files available in both modules and themes.

## Coding Standards on PHP based components

All PHP based components that are not part of the Drupal ecosystem must adhere to the [Symfony][6] standards.
This applies to any library or component that is mainly developed on PHP


[1]: https://www.php-fig.org/psr/psr-1/
[2]: https://www.php-fig.org/psr/psr-2/
[3]: https://www.php-fig.org/psr/psr-4/
[4]: https://github.com/openeuropa/code-review
[5]: https://www.drupal.org/docs/develop/standards
[6]: https://symfony.com/doc/current/contributing/code/standards.html
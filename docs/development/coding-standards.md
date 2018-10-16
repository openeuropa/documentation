# OpenEuropa Coding Standards

OpenEuropa and all its components are built with public contribution in mind. 
In order for all contributions and components to look and feel familiar,
OpenEuropa has agreed on a set of coding standards that all contributors must follow.

Although OpenEuropa does not define any coding standard as such, all the standards it follows
are usually based on well known standards such as [PSR-1][1] and [PSR-2][2].

The following are a list of coding standards guidelines, 
defined using [IETF RFC 2119][3] conformance keywords.

## How to make your code follow the Coding Standards

In order to make it easier for contributors to create new components or to modify existing ones
the [Code Review][4] component has been created.

Coding standards MUST be validated using the OpenEuropa Code Review component
across all different OpenEuropa components.

Please refer to the Code Review [documentation][5] for more information on its usage.

## Coding Standards for Drupal Components

All Drupal based components MUST follow the already defined [Drupal Coding Standards][6].

## Coding Standards for Drupal Themes

Drupal themes are based on the Europa Component Library and should follow the [ECL Coding Standards][7].

## Coding Standards for PHP based components

All PHP based components that are not part of the Drupal ecosystem MUST adhere to the [PSR-2][2] standards.
This applies to any library or component that is mainly developed in PHP.


[1]: https://www.php-fig.org/psr/psr-1/
[2]: https://www.php-fig.org/psr/psr-2/
[3]: https://www.ietf.org/rfc/rfc2119.txt
[4]: https://github.com/openeuropa/code-review
[5]: https://github.com/openeuropa/code-review/blob/master/README.md
[6]: https://www.drupal.org/docs/develop/standards
[7]: https://ec-europa.github.io/europa-component-library/ec/docs/conventions/component

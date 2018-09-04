# Routing system in Drupal 8

When a user visits a particular URL on a Drupal site, the path they are visiting is a route. 
Drupal's routing system helps figure out which [controller][1] is responsible for responding to the route being requested. 
Drupal matches the incoming request's path to a controller by looking through the routes that have been registered in active modules.


## Useful links

- Routing system overview in [drupal.org][2]

    This is the main entry point for Drupal's official documentation about the routing system.
- Symfony's routing component in [symfony.com][3]

    The official documentation for the Symfony routing component that Drupal's routing system is based on.
- Structure of routes in [drupal.org][4]

    This page covers the variety of configuration options that make up routing configuration files.
- Examples project's page_example module [(cgit.drupalcode.org)][5]
The Examples project contains many sub-modules that demonstrate various Drupal sub-systems through well-documented code. 
To learn more about how routing and controllers work, take a look at the page_example module here.


[1]: https://symfony.com/doc/current/controller.html
[2]: https://www.drupal.org/docs/8/api/routing-system/routing-system-overview
[3]: http://symfony.com/doc/current/routing.html
[4]: https://www.drupal.org/docs/8/api/routing-system/structure-of-routes

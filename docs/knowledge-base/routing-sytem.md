# Routing system in Drupal 8

When a user visits a particular URL on a Drupal site, the path they are visiting is a route. 
Drupal's routing system helps figure out which [controller][1] is responsible for responding to the route (URI) being requested. 
Drupal matches the incoming request's path to a controller by looking through the routes that have been registered in active modules.

## Why a new routing system

In prior versions of Drupal, there was only hook_menu. Hook menu actually managed a few different features.
In addition to handling incoming requests, it provided menu links, access control, action links, and a number of other features that are all very tightly coupled together.
By using the Symfony2 Routing component, we are able to split out the route handling aspect, and get a much improved and feature-rich solution.
Such as being able to create routes on more than just the path, for example make a request for JSON, XML or HTML while still using the same path. 


## How the routing system works

Drupal's routing system works with the Symfony HTTP Kernel. 
The routing system is responsible for matching paths to controllers, and you define those relations in routes. You can pass on additional information to your controllers in the route. Access checking is integrated as well.
[See drupal.org][5]

## Structure of routes and parameters

TODO

## Adding new routes (static & dynamic) and altering existing ones


### Adding a new static route

1. In your example.routing.yml (let's use **example** module name as in drupal.org)
    
    Add your path, ( /something )
        and in *defaults:* 
            add the controller class and the method who will do something.
            set a title
        as *requirements:*
            add permission   
        

```
example.content:
  path: '/example' 
  defaults: 
    _controller: '\Drupal\example\Controller\ExampleController::content' 
    _title: 'Hello World'
  requirements: 
    _permission: 'access content' 
```
    

2. In your src/Controller add your page controller class and your methods

```namespace Drupal\example\Controller;

use Drupal\Core\Controller\ControllerBase;

/**
 * An example controller.
 */
class ExampleController extends ControllerBase {

  /**
   * Returns a render-able array for a test page.
   */
  public function content() {
    $build = [
      '#markup' => $this->t('Hello World!'),
    ];
    return $build;
  }
}
```

### Adding a new dynamic route

You can use the alterRoutes() method to add dynamic routes as well. 
A real example can be found in the [configuration translation RouteSubscriber][9].

See [drupal.org][7]

### Altering existing routes

Altering existing routes is done by modifying a **RouteCollection** and using  an **EventSubscriber** triggered by the **RoutingEvents:ALTER** event.

The example use a src/Routing/RouteSubscriber.php file in your module.
Therefore, the class must be registered as an event subscriber service.
Use a example.services.yml file in your module (if the module is named example).
```
services:
  example.route_subscriber:
    class: Drupal\example\Routing\RouteSubscriber
    tags:
      - { name: event_subscriber }
```
[See drupal.org][6]

## Route related objects

Route, CurrentRouteMatch, RouteMatch, Url are objects used for routing in Drupal 8.
-RouteMatch: \Drupal\Core\Routing\RouteMatchInterface
-CurrentRouteMatch: \Drupal\Core\Routing\CurrentRouteMatch

see in [drupal.org][8]

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

- Other ressources:

    https://www.previousnext.com.au/blog/using-drupal-8s-new-route-controllers
    https://befused.com/drupal/routes-controllers


[1]: https://symfony.com/doc/current/controller.html
[2]: https://www.drupal.org/docs/8/api/routing-system/routing-system-overview
[3]: http://symfony.com/doc/current/routing.html
[4]: https://www.drupal.org/docs/8/api/routing-system/structure-of-routes
[5]: https://www.drupal.org/docs/8/api/routing-system/routing-system-overview
[6]: https://www.drupal.org/docs/8/api/routing-system/altering-existing-routes-and-adding-new-routes-based-on-dynamic-ones
[7]: https://www.drupal.org/node/2122201
[8]: https://www.drupal.org/docs/8/api/routing-system/routing-related-objects-route-currentroutematch-routematch-url
[9]: https://api.drupal.org/api/drupal/core%21modules%21config_translation%21src%21Routing%21RouteSubscriber.php/class/RouteSubscriber/8

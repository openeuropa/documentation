# Routing system in Drupal 8

When a user visits a particular URL on a Drupal site, the path they are visiting is a route. 
Drupal's routing system helps figure out which [controller][1] is responsible for responding to the route (URI) being requested. 
Drupal matches the incoming request's path to a controller by looking through the routes that have been registered in active modules.

## Why a new routing system

In prior versions of Drupal, there was only hook_menu. Hook menu actually managed a few different features.
In addition to handling incoming requests, it provided menu links, access control, action links, and a number of other features that are all very tightly coupled together.
By using the Symfony2 Routing component, we are able to split out the route handling aspect, and get a much improved and feature-rich solution.
Such as being able to create routes on more than just the path.
For example, it allows to create routes with different response formats (JSON, XML or HTML) for same path.


## How the routing system works

Drupal's routing system works with the Symfony HTTP Kernel. 
The routing system is responsible for matching paths to controllers, and you define those relations in routes.
You can pass on additional information to your controllers in the route. Access checking is integrated as well.
[See drupal.org: routing-system-overview][5]

## Structure of routes and parameters

The route structure inside the **module.routing.yml** file is described in drupal.org documentation.

REQUIRED PARAMETERS ARE:

* **path** : The URL to the route, with a leading forward slash (e.g., path: '/book'). You can use dynamic properties by including them in curly braces. (e.g., path: '/node/{node}/outline'). These will be passed along as arguments via parameter converters to the controller/form (see below).
* **defaults** : Defines the default properties of a route. Provide one of the following to specify how the output is generated:

    **_controller**: A Callable. This will map to a callable function.

    **_form:** A class name implementing Drupal\Core\Form\FormInterface.

    **_entity_view**: The value is entity_type.view_mode. It will find an entity in the path and render it in the given view mode.

    **_entity_list**: The value is entity_type. It provides a list of entities using the EntityListController of the respective entity.

    **_entity_form**: It is similar to _form, but it will provide an edit form for an entity.

    All title related parameters are OPTIONAL:

    * _title: The page title for the route.
    * _title_arguments: Additional arguments for the title text passed along to t().
    * _title_context: Additional context information for the title text passed along to t().
    * _title_callback: A PHP callable returning the page title for the route.

* **requirements**: Determines what conditions must be met in order to grant access to the route. Is an array of one or more of the following:

    * _permission: A permission string
    * _role: A specific Drupal role, eg. 'administrator'.
    * _access: Set this to 'TRUE'.
    * _entity_access: In the case where an entity is part of a route, can check a certain access level before granting access
    * _custom_access
    * _format: Use this to check the type of the request.
    * _content_type_format: Use this to check the content type of the request.
    * _module_dependencies: Optionally use this key to specify one or more modules that are required to serve this path.
    * _csrf_token: should be used and set to 'TRUE' for any URLs that perform actions or operations that do not use a form callback.

## Adding new routes (static & dynamic) and altering existing ones


### Adding a new static route

1. In your example.routing.yml (let's use **example** module name as in drupal.org)
We can set the title and the path of the route, the used controller class and its method and also to define the permissions.
The resulting JSON will be like this:

```
example.content:
  path: '/example' 
  defaults: 
    _controller: '\Drupal\example\Controller\ExampleController::content' 
    _title: 'Hello World'
  requirements: 
    _permission: 'access content' 
```
    

2. In your src/Controller add your page controller class and your methods.
As basic route controller you can extends Drupal\Core\Controller\ControllerBase.

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

See [drupal.org Providing dynamic routes][7]

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
[See drupal.org altering-existing-routes-and-adding-new-routes-based-on-dynamic-ones][6]

## Route related objects

These objects are used for routing in Drupal 8:

* The __Route__ object is simply the routing YML in PHP form with getters.
* The __RouteMatch_ (\Drupal\Core\Routing\RouteMatchInterface) object contains more relevant information like the name of the route, the route object, the parameters and the raw parameters as relevant for the match but still doesn't have any useful methods either besides getters.
* The __CurrentRouteMatch__ (\Drupal\Core\Routing\CurrentRouteMatch) object is also a RouteMatch but specifically contains the current route object. Again, you can only run getters on this.
* The __Url__ object currently contains the route name, parameters and options for generating the URL. This one has useful methods like getting the system path or a render array.

see in [drupal.org routing-related-objects-route-currentroutematch-routematch-url][8]


## Useful links

- Routing system overview in [drupal.org: routing-system-overview][2]
    This is the main entry point for Drupal's official documentation about the routing system.
- Symfony's routing component in [symfony.com: The Routing component ][3]
    The official documentation for the Symfony routing component that Drupal's routing system is based on.
- Structure of routes in [drupal.org: structure-of-routes][4]
    This page covers the variety of configuration options that make up routing configuration files.
- Examples project's page_example module in [cgit.drupalcode.org/examples/tree][10]
    The Examples project contains many sub-modules that demonstrate various Drupal sub-systems through well-documented code.
    To learn more about how routing and controllers work, take a look at the page_example module here.


[1]: https://symfony.com/doc/current/controller.html
[2]: https://www.drupal.org/docs/8/api/routing-system/routing-system-overview
[3]: hhttps://symfony.com/doc/current/components/routing.html
[4]: https://www.drupal.org/docs/8/api/routing-system/structure-of-routes
[5]: https://www.drupal.org/docs/8/api/routing-system/routing-system-overview
[6]: https://www.drupal.org/docs/8/api/routing-system/altering-existing-routes-and-adding-new-routes-based-on-dynamic-ones
[7]: https://www.drupal.org/node/2122201
[8]: https://www.drupal.org/docs/8/api/routing-system/routing-related-objects-route-currentroutematch-routematch-url
[9]: https://api.drupal.org/api/drupal/core%21modules%21config_translation%21src%21Routing%21RouteSubscriber.php/class/RouteSubscriber/8
[10]: http://cgit.drupalcode.org/examples/tree/
[11]: https://www.previousnext.com.au/blog/using-drupal-8s-new-route-controllers
[12]: https://befused.com/drupal/routes-controllers

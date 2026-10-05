# Routing system

The routing system in Drupal is based on the [Symfony Routing component](https://symfony.com/doc/current/routing.html). It is essentially responsible for mapping user requests to business logic in the site, typically via Controllers.

You can find a basic overview of this system [here](https://www.drupal.org/docs/drupal-apis/routing-system/routing-system-overview).


## How the routing system works

The most common use case of the routing system is defining a route (with a path) that maps to a Controller class. The latter is then responsible for delivering the contents of that page.

A good example of how to do this can be found [here](https://www.drupal.org/docs/drupal-apis/routing-system/introductory-drupal-routes-and-controllers-example).

## Structure of routes

The route definition can contain a lot of information needed in handling the routing, such as access checks. 

A complete list of *keys* you can specify inside a route definition can be found [here](https://www.drupal.org/docs/drupal-apis/routing-system/structure-of-routes).

The most common you will encounter, however, are the following:

* `path` -> the path that needs to be requested to match this route. For more information on how the path can take parameters, read [this](https://www.drupal.org/docs/8/api/routing-system/parameters-in-routes/using-parameters-in-routes)
* `defaults` -> this is where, among other things, the business logic is mapped. Under `defaults` we typically have:
  * `_controller` -> mapping to a fully qualified name of a Controller class or
  * `_form` -> mapping to a fully qualified name of a Form class for a form page
* `requirements` -> contains, among others, access related information that needs to be met for the route to be accessible (such as `_permission`). For more information on access checking on routes, read [this](https://www.drupal.org/docs/8/api/routing-system/access-checking-on-routes).

## Adding dynamic routes

For more complex uses cases, routes can also be declared dynamically, not only via the static `.routing.yml` file. In order to do this, we subscribe to the route building event and provide our definitions dynamically.

In the same way, we can alter route definitions that have already been defined. 

For an example of how to do this, check [here](https://www.drupal.org/docs/drupal-apis/routing-system/altering-existing-routes-and-adding-new-routes-based-on-dynamic-ones).

For more information on the Event Dispatcher and subscribing to events, check out [this entry](https://www.drupal.org/docs/develop/creating-modules/subscribe-to-and-dispatch-events).

## Route related objects

Very often we encounter and have to work with objects that deal with the routing system. The most important are `Request` (and `RequestStack` service), `Route`, `RouteMatch`, `CurrentRouteMatch`, `Url`.

For more information on what these do, check [here](https://www.drupal.org/docs/8/api/routing-system/routing-related-objects-route-currentroutematch-routematch-url)

## Useful links

* [Routing system documentation](https://www.drupal.org/docs/drupal-apis/routing-system) on Drupal.org. 
* The [Render API](https://www.drupal.org/docs/drupal-apis/render-api) documentation describes the internals of transforming a user request into an actual page output.
* Drupal [examples module](https://www.drupal.org/project/examples).

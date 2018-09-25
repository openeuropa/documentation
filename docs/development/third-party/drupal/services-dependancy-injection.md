# Services and Dependency Injection

Dependency injection is a very scary concept in Object Oriented Programming (OOP) but is actually very simple to understand. It is the practice of providing classes or functions with the dependencies they need rather than making them responsible for retrieving them. In other words, and in simple terms, having parameters.

Most typically, dependency injection refers to class constructor dependencies (parameters) that allow objects of that class to perform their functions. In this way, the dependencies can also be swapped.

In more complex applications like Symfony or Drupal, managing these dependencies is done via a `Container` (Service Container in Symfony and Drupal 8). The latter is responsible for collecting objects and their dependencies and making them available to the application when needed (constructing them). It provides the glue between objects, their dependencies and the application.

Check out [this article](https://www.webomelette.com/drupal-8-dependency-injection-service-container-and-all-jazz) for an introduction to dependency injection and the service container.

## What are services in Drupal

Services are objects meant to contain reusable and decoupled functionality. These objects are *registered* with the service container and can be fetched by the application at any point. 

Typically, services are meant to encapsulate the business logic of the application in a decoupled way. In order words, the objective of a service is to "implement" a piece of functionality. And as a consequence of dependency injection, the service can be replaced with another that "implements" the same functionality differently. 

However, services can also be used to contain singular business logic as a way to encapsulate and logically break down functionality. This allows it to also be more easily tested.

## How to define a service

The typical service definition contains a name (something to identify the service) and a class name (the class which gets instantiated by the Container when the service is requested).

Moreover, the service definition typically specifies other services that need to be *injected* into it via the constructor, something that is also handled by the Container. 

For more information on how to define a service, check [here](https://www.drupal.org/docs/8/api/services-and-dependency-injection/structure-of-a-service-file).

## Fetching services

The simplest way to fetch services from the Container is by using the static `\Drupal` class:

```
$service = \Drupal::service('my_service_name');
```

Some services even have accessor shortcuts on the `\Drupal` class. Some notable examples:

```
$entity_type_manager = \Drupal::entityTypeManager();
$database = \Drupal::database();
$config_factory = \Drupal::configFactory();
$logger = \Drupal::logger();
...
```

This method of loading services is static. This means they are fetched from the global scope and therefore are not injected. So it's the least recommended way of accessing services and should only be done from a static
scope such as `.module` or `.install` files. 

## How to inject services in Drupal 8

Instead of accessing the services statically, it's recommended to inject them. And depending on the use case, the injection happens differently.

Check out this [article](https://code.tutsplus.com/tutorials/drupal-8-properly-injecting-dependencies-using-di--cms-26314) for an outline on the most typical use cases of injecting dependencies in Drupal 8 and an explanation of the mechanics behind that.

### In other services

Services may depend on other services for performing their functions. In this case, these dependencies are specified inside the service definition as arguments. The latter are then passed by the Container and *received* by the service via the constructor.

### In controllers (and forms)

Controllers are the typical entry point for creating pages in Drupal 8. They extend `ControllerBase` which already provides some methods for accessing common and any other services. However, using these directly **is not dependency injection** as it is handled statically.

Instead, we should use the `create()` method of the `ContainerInjectionInterface` to *ask* the container for the services we need and then *receive* them in the constructor. See [here](https://code.tutsplus.com/tutorials/drupal-8-properly-injecting-dependencies-using-di--cms-26314) the `Controllers` heading for an example and explanation on how this works internally.

In Form classes, the process is exactly the same. See [this entry]() for more information on the Form API (@todo add link).

### In plugins

Plugins are slightly more complicated as they receive some extra arguments from the plugin manager when they are instantiated (they are not resolved like the controllers). But the concept is similar. See [here](https://code.tutsplus.com/tutorials/drupal-8-properly-injecting-dependencies-using-di--cms-26314) the `Plugins` heading for an example and explanation on how this works internally.

### Where we cannot inject services

Dependency injection should be used (instead of static service fetching) whenever possible. However, there are a few exceptions where this is not possible:

* Static files (such as `.module` or `.install`)
* `FieldType` plugins which are not container aware

## Where can we quickly find existing core services?

Drupal core comes with loads of services that can and should be used. These are defined typically in two places:

* Individual core module `.services.yml` files
* The `core.services.yml` file

These are the quick reference points for service definitions that can be used as dependencies for custom services.

## Tagged services and service collectors

Service tags are used to specify that a given service is used (collected) by a subsystem or belongs to a category. 

Popular examples of tagged services are the event subscriber services which are collected by the event dispatcher and registered as listeners to specific events. For more information on the event dispatcher, read [this entry]() (@todo add link).

For an example of how a tagged based service collector works, read [this](https://www.drupal.org/docs/8/api/services-and-dependency-injection/service-tags).

## Dynamic services and altering existing ones

Apart from the static definition inside `.services.yml` files, services can also be declared dynamically. This is done by implementing a specially named class and altering the `ContainerBuilder`.

At this point new service definitions can be added and existing ones altered. See [here](https://www.drupal.org/docs/8/api/services-and-dependency-injection/altering-existing-services-providing-dynamic-services) for an example on how to do this.

## Useful links

* [Services and dependency injection in Drupal 8](https://www.drupal.org/docs/8/api/services-and-dependency-injection/services-and-dependency-injection-in-drupal-8) on Drupal.org

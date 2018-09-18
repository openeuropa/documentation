# What is dependency injection and how it works in the wild
# What is a service and why use services (and why not statically load them via \Drupal::service())
# How to define a service
## Tagged services and service collectors
# How to inject services in Drupal 8
## In other services
## In controllers (and forms)
## In plugins
## Where can we not inject services?
# Where can we quickly find existing core services?
# Altering services



# Core services

In Drupal 8 speak, a service is any object managed by the services container.
Drupal 8 introduces the concept of services to decouple reusable functionality and makes these services pluggable and replaceable by registering them with a *service container*.

As a developer, services are used to perform operations like accessing the database or sending an e-mail.
Rather than use PHP's native MySQL functions, we use the core-provided service via the service container to perform this operation so that our code can simply access the database without having to worry about whether the database is MySQL or SQLlite, or if the mechanism for sending e-mail is SMTP or something else.

Core services are defined in CoreServiceProvider.php and core.services.yml.

A service container (or dependency injection container) is a PHP object that manages the instantiation of services. Drupal's service container is built on top of the Symfony service container.
Documentation on the structure of this file, special characters, optional dependencies, etc. can all be found in the Symfony service container documentation.

Services sound a lot like PHP objects, except that we specify them via configuration, instead of code.
But there's more to it than meets the eye.
Services are instantiated lazily, which means no service object is created if the service is not invoked.
The other difference is, the same object is returned every time you invoke the service instead of creating new instances.

Attention Services and Plugings are not the same:
Plugins are reusable objects discoverable by *annotations*. Though they are similar to services by definition, they differ in many ways.
If you want to expose an interface which can exhibit different behaviour, go for a plugin.


# Services and Dependency Injection

Symfony uses a service container that can be used to efficiently manage services in the application. This concept is also known as *Dependency Injection*.
This Service Container* is a global object that is created and contained by the Kernel before a request is handled. It can be used later in code to fetch services, lazy-loaded on the fly.
Services are global objects that can be used to fulfil specific tasks, such as a Mailer service, or a database connector. A service corresponds to exactly one class.
The service container is very important as it contains the available services, knows about their relations and configurations, and even constructs them!


## Why dependency

A service may depend on other services. The Symfony documentation uses the example of a NewsletterManager service that needs a Mailer service to actually send the emails.
These dependencies are also managed in the Service Container. When creating a service, his dependencies are supplied via arguments in the class constructor.
Interfaces are used to define which methods the dependent services should provide, so that the service implementation can be swapped with another one when necessary.


## The injection

Dependency injection is the preferred method for accessing and using services in Drupal 8 and should be used whenever possible.

Passing in the services an object depends on explicitly is called dependency injection. In several cases, dependencies are passed explicitly in class constructors of the controller.
By the routing process, the controller will use services to display content (responses)


## Defining your own services

You can define your own services using an example.services.yml file, where example is the name of the module defining the service.
This file uses the same structure as the core.services.yml file.

```
services:
module_name.service_name:
class: Drupal\module_name\ClassOfTheService
```

You can use drupal console command to generate a blueprint in your module and then add things for your specific usecase.
```
drupal generate:service
```
or create file by yourself.

Then inside your service class you add all the method needeed to accomplish the responsability of this service.


## Using your services

Exemple:
Given you have a _listbook_ service registered in your services container with a method to list all books.
Then in your controller method routed with _/my_books_ you can call/use the service like this:

```
$book_list = \Drupal::service('mymodule.listbooks')->getBooks();
```


## Ressources

[drupal.org][1]

[Symfony/service_container][2]

[Symfony/dependancy_injection][3]


[1]:https://www.drupal.org/docs/8/api/services-and-dependency-injection/services-and-dependency-injection-in-drupal-8
[2]:https://symfony.com/doc/current/service_container.html
[3]:https://symfony.com/doc/current/components/dependency_injection.html

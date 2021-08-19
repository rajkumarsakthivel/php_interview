Service Container
=================
The Laravel service container is a powerful tool for managing class dependencies and performing dependency injection. Dependency injection is a fancy phrase that essentially means this: class dependencies are "injected" into the class via the constructor or, in some cases, "setter" methods.

Service providers:
=================
Service providers are the central place of all Laravel application bootstrapping. Your own application, as well as all of Laravel's core services, are bootstrapped via service providers.

But, what do we mean by "bootstrapped"? In general, we mean registering things, including registering service container bindings, event listeners, middleware, and even routes. Service providers are the central place to configure your application.

Middleware:
===========
provide a convenient mechanism for inspecting and filtering HTTP requests entering your application.

Collection:
===========
class provides a fluent, convenient wrapper for working with arrays of data

Laravel's "contracts":
=====================
are a set of interfaces that define the core services provided by the framework.

Laravel's events:
=================
provide a simple observer pattern implementation, allowing you to subscribe and listen for various events that occur within your application

MySQL
=====
INNER) JOIN: Returns records that have matching values in both tables
LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table

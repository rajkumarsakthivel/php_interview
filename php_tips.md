# PHP 7:

https://www.quora.com/What-are-the-major-difference-between-PHP-5-and-PHP-7

# Cookie:
setcookie("TestCookie", "", time() - 3600, "/~rasmus/", "example.com", 1);
bool setcookie ( string $name [, string $value = "" [, int $expire = 0 [, string $path = "" [, string $domain = "" [, bool $secure = false [, bool $httponly = false ]]]]]] )

# HTTP STATUS CODES:

1xx Informational

100 Continu

# 2xx Success

200 OK

201 Created

204 No Content

# 3xx Redirection

304 Not Modified

# 4xx Client Error

400 Bad Request

401 Unauthorized

403 Forbidden

404 Not Found

405 Method Not Allowed

409 Conflict

# 5xx Server Error

500 Internal Server Error

# Top Ten Reasons To Use Laravel:

Excellent Documentation.

Laracasts

Intuitive Syntax

Practical Application Structure

Artisan Code Generation

Out-of-the-box User Model

Blade Templating Engine

Dependency Injection Made Simple

Supporting Products and Packages

Innovative Founder

Laravel is a very popular PHP framework, used by more than 30,000 developers around the world. 
One of the reasons it’s such a hit is that it allows web applications to be constructed quickly 
and makes them easy to maintain afterwards.

The source code for Laravel is hosted on GitHub and is distributed under an open source licence, so it’s available for anyone to use.
It was first introduced in beta in 2011 and has since gone through several enhancements adding more features including
database seeding, scheduling and more besides.

The third version of the platform saw the introduction of a command line interface called Artisan.
This is mapped to sub-commands which simplifies the process of building and managing Laravel-based apps.

It works on a modular basis, with lots of pre-built functions available. This means that applications can be constructed quickly
with no need for hours of work and lots of lines of code. Things like form validation and user authentication are 
built into Laravel which means they don’t need to be reinvented for each new task.

The code is designed to be simple, readable and elegant, making it easy for developers to understand what’s happening 
even if the code was created by someone else. Testing is integrated into the Laravel framework too, so the resource 
intensive business of writing test procedures for each new task is reduced too.

Recent additions to the platform include Laravel Scout which allows full text searches to be performed; Laravel 
Echo which allows for event broadcasting over the web; and Laravel Passport which is an OAuth2 ready server that
makes API authentication simpler.

Another reason for the popularity of the platform is its thriving and helpful developer community. 
There’s a plethora of documentation available which means developers have plenty to guide them 
when it comes to applying best practices, making decisions on implementation, and maintaining code. 

## What has changed in Zend Framework 2 from Zend Framework 1?

###### Architecture

ZF1 is based on MVC , ZF2 is based on MOVE. Huge difference. MOVE = Model Operations Views Events , MVC = Models Views Controllers. More here. Zend Framework 2 uses 100% object-oriented code and utilises most of the new features of PHP 5.3, namely namespaces, late static binding, lambda functions and closures. source

###### Size of installation

The latest ZF1 file is approx 30Mb and ZF2 is approx 2.5Mb (Zipped).

###### Dependency

ZF1 is core set of libraries and very loosely coupled architecture (with respect to its competitor/player - CakePHP). ZF1 does not require much of 'gems' (as in ruby) but, can do better with plugins. ZF2 requires you to know about composer - phar and soon it may out-match any other framework. New concept : Dependency Injection for Zend fans.

###### Certification

Certification is available only for ZF1, however, there are rumours about their talks for ZF2 certs though training material is available online.

###### Conventions
classname in ZF1 was Zend_Db_Table for class in Zend/Db/Table.php whereas in ZF2, it is class My\Auth\Adapter . Enough said.

###### Rest Api
Use HTTP Verbs to Make Your Requests Mean Something
API consumers are capable of sending GET, POST, PUT, and DELETE verbs, which greatly enhance the clarity of a given request.

Generally, the four primary HTTP verbs are used as follows:

GET
Read a specific resource (by an identifier) or a collection of resources.
PUT
Update a specific resource (by an identifier) or a collection of resources. Can also be used to create a specific resource if the resource identifier is know before-hand.
DELETE
Remove/delete a specific resource by an identifier.
POST
Create a new resource. Also a catch-all verb for operations that don't fit into the other categories.
Note
GET requests must not change any underlying resource data. Measurements and tracking which update data may still occur, but the resource data identified by the URI should not change.

Provide Sensible Resource Names
Producing a great API is 80% art and 20% science. Creating a URL hierarchy representing sensible resources is the art part. Having sensible resource names (which are just URL paths, such as /customers/12345/orders) improves the clarity of what a given request does.

Appropriate resource names provide context for a service request, increasing understandability of the API. Resources are viewed hierarchically via their URI names, offering consumers a friendly, easily-understood hierarchy of resources to leverage in their applications.

Here are some quick-hit rules for URL path (resource name) design:

Use identifiers in your URLs instead of in the query-string. Using URL query-string parameters is fantastic for filtering, but not for resource names.
Good: /users/12345
Poor: /api?type=user&id=23
Leverage the hierarchical nature of the URL to imply structure.
Design for your clients, not for your data.
Resource names should be nouns. Avoid verbs as resource names, to improve clarity. Use the HTTP methods to specify the verb portion of the request.
Use plurals in URL segments to keep your API URIs consistent across all HTTP methods, using the collection metaphor.
Recommended: /customers/33245/orders/8769/lineitems/1
Not: /customer/33245/order/8769/lineitem/1
Avoid using collection verbiage in URLs. For example 'customer_list' as a resource. Use pluralization to indicate the collection metaphor (e.g. customers vs. customer_list).
Use lower-case in URL segments, separating words with underscores ('_') or hyphens ('-'). Some servers ignore case so it's best to be clear.
Keep URLs as short as possible, with as few segments as makes sense.
Use HTTP Response Codes to Indicate Status
Response status codes are part of the HTTP specification. There are quite a number of them to address the most common situations. In the spirit of having our RESTful services embrace the HTTP specification, our Web APIs should return relevant HTTP status codes. For example, when a resource is successfully created (e.g. from a POST request), the API should return HTTP status code 201. A list of valid HTTP status codes is available here which lists detailed descriptions of each.

Suggested usages for the "Top 10" HTTP Response Status Codes are as follows:

200 OK
General success status code. This is the most common code. Used to indicate success.
201 CREATED
Successful creation occurred (via either POST or PUT). Set the Location header to contain a link to the newly-created resource (on POST). Response body content may or may not be present.
204 NO CONTENT
Indicates success but nothing is in the response body, often used for DELETE and PUT operations.
400 BAD REQUEST
General error for when fulfilling the request would cause an invalid state. Domain validation errors, missing data, etc. are some examples.
401 UNAUTHORIZED
Error code response for missing or invalid authentication token.
403 FORBIDDEN
Error code for when the user is not authorized to perform the operation or the resource is unavailable for some reason (e.g. time constraints, etc.).
404 NOT FOUND
Used when the requested resource is not found, whether it doesn't exist or if there was a 401 or 403 that, for security reasons, the service wants to mask.
405 METHOD NOT ALLOWED
Used to indicate that the requested URL exists, but the requested HTTP method is not applicable. For example, POST /users/12345 where the API doesn't support creation of resources this way (with a provided ID). The Allow HTTP header must be set when returning a 405 to indicate the HTTP methods that are supported. In the previous case, the header would look like "Allow: GET, PUT, DELETE"
409 CONFLICT
Whenever a resource conflict would be caused by fulfilling the request. Duplicate entries, such as trying to create two customers with the same information, and deleting root objects when cascade-delete is not supported are a couple of examples.
500 INTERNAL SERVER ERROR
Never return this intentionally. The general catch-all error when the server-side throws an exception. Use this only for errors that the consumer cannot address from their end.

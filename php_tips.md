# PHP 7:
https://blog.feryn.eu/php-7-is-now-available-new-features-improvements/

# Cookie:
setcookie("TestCookie", "", time() - 3600, "/~rasmus/", "example.com", 1);

# HTTP STATUS CODES:
1×× Informational

100 Continue

101 Switching Protocols

102 Processing

2×× Success

200 OK

201 Created

202 Accepted

203 Non-authoritative Information

204 No Content

205 Reset Content

206 Partial Content

207 Multi-Status

208 Already Reported

226 IM Used

3×× Redirection

300 Multiple Choices

301 Moved Permanently

302 Found

303 See Other

304 Not Modified

305 Use Proxy

307 Temporary Redirect

308 Permanent Redirect

4×× Client Error

400 Bad Request

401 Unauthorized

402 Payment Required

403 Forbidden

404 Not Found

405 Method Not Allowed

406 Not Acceptable

407 Proxy Authentication Required

408 Request Timeout

409 Conflict

410 Gone

411 Length Required

412 Precondition Failed

413 Payload Too Large

414 Request-URI Too Long

415 Unsupported Media Type

416 Requested Range Not Satisfiable

417 Expectation Failed

418 I'm a teapot

421 Misdirected Request
422 Unprocessable Entity
423 Locked
424 Failed Dependency
426 Upgrade Required
428 Precondition Required
429 Too Many Requests
431 Request Header Fields Too Large
444 Connection Closed Without Response
451 Unavailable For Legal Reasons
499 Client Closed Request
5×× Server Error
500 Internal Server Error
501 Not Implemented
502 Bad Gateway
503 Service Unavailable
504 Gateway Timeout
505 HTTP Version Not Supported
506 Variant Also Negotiates
507 Insufficient Storage
508 Loop Detected
510 Not Extended
511 Network Authentication Required
599 Network Connect Timeout Error

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

######Architecture

ZF1 is based on MVC , ZF2 is based on MOVE. Huge difference. MOVE = Model Operations Views Events , MVC = Models Views Controllers. More here. Zend Framework 2 uses 100% object-oriented code and utilises most of the new features of PHP 5.3, namely namespaces, late static binding, lambda functions and closures. source

######Size of installation

The latest ZF1 file is approx 30Mb and ZF2 is approx 2.5Mb (Zipped).

######Dependency

ZF1 is core set of libraries and very loosely coupled architecture (with respect to its competitor/player - CakePHP). ZF1 does not require much of 'gems' (as in ruby) but, can do better with plugins. ZF2 requires you to know about composer - phar and soon it may out-match any other framework. New concept : Dependency Injection for Zend fans.

######Certification

Certification is available only for ZF1, however, there are rumours about their talks for ZF2 certs though training material is available online.

######Conventions
classname in ZF1 was Zend_Db_Table for class in Zend/Db/Table.php whereas in ZF2, it is class My\Auth\Adapter . Enough said.

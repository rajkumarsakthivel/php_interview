abstract class:
===============
you cannot create instance for abstract class.
you can extend abstract class and create instance for the extending class
All the methods marked as abstract should be defined in the extending class
all the visible methods that are not marked as abstract are available in the extending class (child class) 

An abstract class is a class that you cannot create an instance of. It can provide basic functionality, but in order for that 
functionality to be used, one or more other classes must derive from the abstract class. One of the major benefits of 
abstract classes is that you can reuse code without having to retype it. That has a plethora of benefits, such as reducing
bugs and making coding faster. A concrete example of an abstract class would be a class called Animal. 
You see many animals in real life, but there are only kinds of animals.
That is, you never look at something purple and furry and say "that is an animal and there is no more specific way of defining it".
Instead, you see a dog or a cat or a pig... all animals. The point is, that you can never see an animal walking around that isn't more 
specifically something else (duck, pig, etc.). The Animal is the abstract class and Duck/Pig/Cat are all classes that derive 
from that base class. Animals might provide a function called "Age" that adds 1 year of life to the animals. 
It might also provide an abstract method called "IsDead" that, when called, will tell you if the animal has died. 
Since IsDead is abstract, each animal must implement it. So, a Cat might decide it is dead after it reaches 14 years of age,
but a Duck might decide it dies after 5 years of age. The abstract class Animal provides the Age function to all classes 
that derive from it, but each of those classes has to implement IsDead on their own.

Interfaces:
===========
Interfaces are a type of abstract classes.
In interfaces you cannot define methods. Only function declaration without function body is allowed.
All the methods declared in an interface should be defined by the class implementing that interface
A class can implement multiple interfaces (This effectively implements multiple inheritance in php)

an interface is like an abstract class, except it does not contain any logic. Rather, it specifies an interface. So, there
might be an interface called IFly. This might have the methods GoForward and GoDown. Those methods would not actually 
contain any logic... each class that implements interface IFly would have to implement those GoForward and GoDown methods. 
You could have classes Duck and Finch implement interface IFly.
Then, if you want to keep a list of instances that can fly, you just create a list that contains items of type IFly.
That way, you can add Ducks and Finches and any other instance of a class the implements IFly to the list.

So, abstract classes can be used to consolidate and share functionality, while interfaces can be used to specify
what the common functionality that will be shared between different instances will be, without actually building that
functionality for them. Both can help you make your code smaller, just in different ways. There are other differences 
between interfaces and abstract classes, but those depend on the programming language, so I won't go into those other differences here.

constructor & destructor:
============
Constructor is a magic method which is invoked at the time of creating an instance of a class.

destructor is a magic method which is invoked at the time of destruction of an instance of a class.

Inheritance:
============
Inheritance is an oops concept. when a parent class has a public or protected method or property, it is available in its child class without defining inside child class.

static:
=======
if a method is defined as static, it can be called without creating an instance of the class using scope resolution operator ::

class constants are always statically called.

autoloading classes:
====================
__autoload is a magic method. This method is called by php when a non existent classes in a php script.
The name of the class is sent as an argument to this method and it can include the class. reference: http://www.php.net/manual/en/language.oop5.autoload.php

visibility:
===========
public: properties and methods are visible everywhere.
protected: properties and methods are visible at the same class and child classes
private: properties and methods are visible at the same class alone.

if you try to access protected / private property or method in the instance of the class like the following, you will get fatal error
echo $obj->protected; // Fatal Error
echo $obj->private; // Fatal Error

refernce: http://www.php.net/manual/en/language.oop5.visibility.php

overloading:
============

creating methods and properties at runtime is called property overloading / method overloading.
In php, property overloading can be done by magic methods like __set, __unset, __isset, __get
method overloading can be done by magic methods like __call and __call_static

                                             
magic methods
=============
magic methods are functions that are call not by the user by php itself at runtime at certain events.
examples: __call, __set, __unset, __autoload, __construct, __destruct, __sleep, __wakeup etc.

polymorphism:
============
polymorphism means "having multiple forms"
a same method or property can behave differently at different situations.
for example, animal class can have a method called speak().
when a class called cat extends animal, the class will return "meow" when you call speak()
when a class called dog extends animal, the class will return "wow wow!!" when you call speak()
etc

Credits: Poomalairaj

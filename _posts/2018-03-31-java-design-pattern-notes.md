---
title: Java  Design Pattern Notes
---

* TOC
{:toc}

Creational
=====

Singleton
-----
* Constructor is private and takes no argument
* Create with "getInstance()" method
* Not interface driven, not easy to unit test

Builder
-----
* Immutability
* Example: StringBuilder
* Telescoping (recursive constructor) not flexible
* builder.bread("wheat").dressing("mayo");
* in class, return this

Prototype
-----
* Typically doesn't use "new"
* Usually implemnted with a Registry
* Example: java.lang.Object#clone()
* Shallow or Deep Copy
* Great to set default values in Registry.create method

Factory
-----
* Opposite of Singleton
* Example: Calendar

Abstract Factory
-----
* Factory of Factories
* Hides the Factory
* Abstracts Environment
* Built through Composition
* Framework pattern

Structural
=====

Adapter
-----
* Multiple Adapters
* Don't add functionality - consider decorator
* Retrofitted

Bridge
-----
* Designed upfront for uncertainty and flexibility
* Abstraction and implementation vary
* Built in advance and complex. 
* Utilizes composition, but more.

Composite
-----

Decorator
-----
* Doesn't change underlying object (Base object can stay same )
* Modifies (adds) behavior
* New class for every feature added
* Often confuised with simple inheritance

Facade
-----

Flyweight
-----

Proxy
-----

Behavioral
=====

Extra
-----
* "If pattern includes another pattern, it's framework"

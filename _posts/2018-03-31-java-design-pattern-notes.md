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

Composite
-----

Decorator
-----

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

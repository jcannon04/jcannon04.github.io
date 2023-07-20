# Object Oriented Principles

## Inheritance:

Inheritance is a mechanism in OOP that allows a class to inherit properties and behaviors from another class. The child class can access and use the attributes and methods defined in the parent class. Inheritance promotes code reuse, modularity, and hierarchical organization of classes. It enables the creation of specialized classes that inherit common characteristics from a more general class. Inheritance is represented using an "is-a" relationship, where the child class is a specific type of the parent class.

## Abstraction:

Abstraction is the process of simplifying complex systems by focusing on essential characteristics while hiding unnecessary details. In OOP, abstraction is achieved through abstract classes and interfaces. An abstract class is a blueprint for other classes and cannot be instantiated itself. It may contain abstract methods (without implementation) and concrete methods (with implementation). Abstract methods act as placeholders, defining a method's signature but leaving the implementation to the derived classes. Interfaces, on the other hand, define a contract of methods that implementing classes must adhere to. Abstraction helps in creating modular and loosely coupled systems by defining common behavior without specifying implementation details.

## Polymorphism:

Polymorphism allows objects of different classes to be treated as objects of a common superclass during runtime. It enables a single interface to be implemented by multiple classes, each providing its own specific implementation. Polymorphism promotes code flexibility and extensibility, as it allows methods to be written to accept objects of a superclass, and these methods can work with objects of any subclass of that superclass. Polymorphism can be achieved through method overriding and method overloading. Method overriding occurs when a subclass provides its own implementation of a method already defined in the parent class. Method overloading occurs when multiple methods with the same name but different parameters are defined in a class. The appropriate method is selected based on the arguments passed during runtime.
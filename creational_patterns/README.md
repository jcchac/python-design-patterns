# Creational patterns

Creational patterns are design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

## Singleton

The Singleton pattern lets ensure that a class has only a single instance, while providing a global access point to it. 

1. **Ensure that a class has only a single instance:** allows to control the access to some shared resources, for example a database or a file.

2. **Global access point:** the object can be access from anywhere in the program, while protecting the instance from being overwritten.

### :balance_scale: Pros and Cons

:heavy_check_mark: Ensures that a class has only a single instance.

:heavy_check_mark: A global access point to that instance is provided.

:heavy_check_mark: The singleton object is initialized only when it's requested for the first time.

:x: Violates the Single Responsability Principle (SRP), as it solves two problems at a time.

:x: Can mask bad design, for example when some components know too much about others.

:x: Breaks modularity of code and its considered an antipattern by many developers, so its usage is on the decline in Python code.

:x: Requires special treatment in multithreaded environments, so that multiple threads don't create a singleton object several times.

:x: Its difficult to unit test the client code of the Singleton because many test frameworks rely on inheritance when producing mock objects. Since the constructor of the Singleton class is private and overriding static methods is impossible in most languages, a creative way to mock the singleton will be required.


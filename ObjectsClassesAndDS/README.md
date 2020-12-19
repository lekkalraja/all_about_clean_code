## Classes, Objects & Data Structures

* `Clean Code` : Write code which is readable & easy to understand
* `Patterns & Principles` : Write code which is maintainable and extensible

#### The Difference between Objects & Data structures
##### Object
* Private internals/properties, public API (methods)
* Contain your business logic (in OOP)
* Abstractions over concretions
##### Data Container/ Data Structure
* Public internals/properties (almost) no API (methods)
* Store and transport data
* Concretions only

* Classes should be small
* Typically should prefer many small classes over a few large classes
* Classes should have a single responsibility (`Single-Responsibility Principle (SRP)`)
* A Product class is responsible for product 'issues' (e.g. change the project name, create, update & remove prodjct etc...)

### Cohesion
* How much are your class methods using the class properties ?
* `Maximum Cohesion` : All methods each use all properties . A Highly Cohesive object
* `No Cohesion` : All methods don't use any class properties. Data structure/ container with utility methods.

### Law Of Demeter
* Principle of Least Knowledge: Don't depend on the internals of "strangers" (other objects which you don't directly know) unless it is Data Structures/containers
* Code in a method may only access direct internals (properties and methods) of:
  * the object it `belongs to`
  * objects that are `stored in properties of that object`
  * objects which are `received as method parameters`
  * objects which are `created in the method`
#### Tell, Don't ASK

## The SOLID Principles

* `S : Sinple Responsibility Principle` :
      * Classes should have a `single responsibility` - a class shouldn't change for more than one reason
      * Restricting classes to one core responsibility leads to smaller classes
      * Smaller classes tend to be easier to read
* `O : Open-Closed Principle` :
      * A class should be open for extension but closed for modification
      * Extensibility ensures small class (instead of growing classes) and can help prevent code duplication (DRY)
      * Smaller classes and DRY code increase readability and maintainability
* `L : Liskov Substitution Principle` :
      * Objects should be replaceable with instances of their subclasses without altering the behavior.
* `I : Interface Segregation Principle` :
      * Many Client-Specific interfaces are better than one general purpose interface.
* `D : Dependency Inversion Principle` :
      * You should depend upon abstractions, not concretions.
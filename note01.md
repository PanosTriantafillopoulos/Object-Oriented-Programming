# Object Oriented Programming Notes 1

The following is a collection of my notes from this unit.

## Definitions
- Object Oriented Programming: Programming paradigm that focuses on the creation of custom classes for special objects
- Class: An abstract description of a new object that can be made. Classes contain attributes and methods
- Attribute: Variables/Data that belongs to the class
- Method: Functions that the object can use and call for computation
- Object: An instance of a class that can be used within a program. An object may have access to the attributes and methods for that class. 
- Encapsulation (Information Hiding):
- Inheritance: Restricting the access to the classes/objects’ certain attributes and methods.
- Single Inheritance: A subclass inheriting the features of a single superclass / parent class
- Multiple Inheritnace: A subclass inheriting the features of  multiple parent classes
- Multilevel Inheritance: A subclass is inheriting from another subclass.
- Polymorphism: A method that can be used across different classes and object that is dependent on the parameters.
- Overloading: Two methods in one class that have the same method name, but different parameters
- Overriding: Two methods with the same method name and parameters.

## Slideshow #1 (U3L1)


## Slideshow #2 (U3L2)
| Topic | Further Description |
| ----- | ------------------- |
|Encapsulation (Information Hiding): Restricting the access to the classes/objects’ certain attributes and methods.|Data protectionRestricting certain methods to be callable Common Practice: have a setter and a getter when all attributes are encapsulated. We should have our attributes encapsulated. If something is not encapsulated a third party may be altered if it is not hidden. We need a setter and a getter to access the encapsulated attribute. Setter and getter are public methods. Setter gets to control how we update the attribute. We only need these if our attributes are encapsulated. Setter controls how the attributes are updated. To see what the value is, use the getter method.|
|Overloading|Two methods in one class with the same method name, but different parameters. This is illegal in python. Ex. show() vs. show(arg)
|Overriding|Two methods with the same method name and parameters. Ex. class A: .sort() class B: .sort(). One method is in the parent class. One method is in the child class Overriding allows the child class to provide a specific implementation for a method that exists in the parent class. You can also override the built-in magic-method. OR Base-functions.|
|Polymorphism|A method that can be used across different classes and objects that is dependent on the parameters. Different Classes (non-inherited) can have the same named methods → Polymorphism. Within a set of inherited classes have the same methods.|

✔️Override and Polymorphism
We can have:
Two different classes that have a same attribute and methods
A child of a parent have an overridden method where the child would utilize the method differently.


✔️Why override built-in methods and operators
Benefits:
Can start to complete mathematical operations on custom Objects
Can start to compare equality between custom objects
Therefore: You can start to manipulate how the object behaves when met with built-in methods nad operators.


## Slideshow #3 (U3L3)



##Sidenotes and Small Important Details
- Class is a keyword that allows to create our own classes.
- Double Underscores? These are key hidden features of Python that allow us to do some overwriting of Python features and hidden content
- Initilization:
```python

```
- str stuff: 
```python

```

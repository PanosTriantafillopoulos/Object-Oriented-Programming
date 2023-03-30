# Object Oriented Programming Notes 1

The following is a collection of my notes from the Object Oriented Programming unit.

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
| Topic | Further Description |
| ----- | ------------------- |
| Object | In CS: Object can be a variable, a data structure, a function, or a method; therefore, a location in memory having a value that can be referenced by an identifier In OOP: Similar to an object as in CS, an object in OOP is an instance of a class where this object can be either a variable, a function, a data structure or a combination of such.|
| Object Oriented Programming (OOP) | Programming practice to design modular reusable software systems, OOP designs programs with creation of Objects, An approach that focuses on the definition of data rather than the input → processing → output logic (OOP vs procedure-oriented programming), The goal is to create an object that we can define and provide functionality to solve problems. |
```python
# Example class
class Person:
  def __init__(self, name):
		self.name = name
	#end of initialization
	
  def greet(self): # the self parameter is always required
		print(“Hello, my name is”, self.name)
	#end of greet
#end of class Person
```


✔️In-depth Analysis of an Object

__Reminder__: An object is an instance

States: The characteristic, Measurable data of an object

Behaviours: The available functionality of the object (what can it do?)
Note: We call an objects data attributes and we call an objects code methods. 

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
| Topic | Further Description |
| ----- | ------------------- |
| Inheritance | When an object or class is based on another class; where its features are from a parent class. Inheritance can have an hierarchy (branching like a tree) and/or be a hybrid: mixing the types of inheritances. Types: Single, Multiple, Multilevel|
| Super() | is a built-in method for classes to refer their parent class. This prevents us from doing ParentClass.method(self)|
| Polymorphism | Ideas: Different Classes (non-inherited) can have the same named methods (Simple) → Polymorphism Within a set of inherited classes have the same methods |

✔️What can we do with Inheritance?
- A child will receive all attributes and methods of the parent
- A child can then enhance itself with new attributes and new methods
- A child can OVERRIDE attributes and methods for their own liking/speciality

✔️ Types of Multiple Inheritances
1. Multi-Generational: Grandparent → Parent → Child
2. Multi-Parent (Not limited to two)
3. Mixture of 1 and 2

```python
# Inheritance Example
#Parent
class Person:
  def __init__(self, name):
  	self.__name = name 
  
  def getName(self):
    return self.__name
#Inherited Class
class Student(Person):
  def __init__(self, name, num):
    Person.__init__(self, name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" % (self.__sNum,self.getName()))
```

## Slideshow 4 (U3L4)
| Topic | Further Description |
| ----- | ------------------- |
| Iterable Objects | Objects that we can iterate through like a sequence. (like strings and lists). To access values without indexing we used a for loop. The portion of the iterable object must be a sequence. Iterable doesn’t always mean indexable.
| __ iter __() | Allows our object to be iterable, when invoked upon (ex. By a for loop), it will call the method. Commonly just returns itself. |
| __ next __() | Allows us to get to the next value when we iterate through a sequence. |
```python
# Example usage of iter and next
class Deck:
	...Code...
	def __iter__(self):
		return self
	def __next__(self):
		self.__index += 1
		if self.__index == len(self.__cards):
			self.__index = -1
			raise StopIteration
		else:
			return self.__cards[self.__index]
	...Code...
```

### Sidenotes
Class is a keyword that allows to create our own classes.
- Create a class:
1. First define the name of the class with the keyword: class
2. In its code block (indentation) define its attributes
3. Then you can assign a variable with an instantiation of the class to interact with it
Make sure to use parentheses when calling the class name.


- Conceptual Differences:
-OOP focuses on how to manipulate the data of the object rather than the logic required to manipulate them-

Procedure Oriented
A human may require:
- Calculations
- Logical Evaluations
- Complete Repetitive Tasks
- Database

OOP
Creating a human object
- What's their name
- What's their address
- What functions can this object have?




- Double Underscores? These are key hidden features of Python that allow us to do some overwriting of Python features and hidden content
- Initilization:
```python
def __init__(self):
```
The initialization method is executed as soon as an object of the class is instantiated.
It helps us to do any initialization for the object’s attributes.
self parameter is used to denote that the method is applied and accessible for the object itself.
self will also treat its own attributes as local.
- str stuff: 
```python
# Example of __str__ and _repr__ methods that allow to express our objects are string outputs.
def __str__(self):
        return f"Point Objct: ({self.x}, {self.y})"
def __repr__(self):
        return self.__str__()
```
__repr__ → Allows us to present a printable version of our object

__str__ → Allows us to convert our object to a string

If a child class inherits the parent class:
The child does not need a new __init__() method UNLESS it requires new attributes.
The child does not need to reinstate the parent’s methods UNLESS you override them.

Encapsulation is denoted by double underscores in the front of an attribute.

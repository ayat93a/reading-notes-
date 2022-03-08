# object-oriented programming
paradigms of programming :
- imperative (using statements, loops, and functions as subroutines)
- functional (using pure functions, higher-order functions, and recursion) 
-  object-oriented programming (OOP)
--> Classes and objects are the two main aspects of object-oriented programming.\
--> Objects are created using classes,The class describes what the object will be, but is separate from the object itself. In other words, a class can be described as an object's blueprint. \
You can use the same class as a blueprint for creating multiple different objects.\
Classes are created using the keyword class and an indented block, which contains class methods (which are functions).\

==> In Python, everything is an object – integers, strings, lists, functions, even classes themselves. Python hides the object machinery with the help of special syntax.

## Create a Class
To create your own custom object in Python, you first need to define a class using the keyword  --> `class`\
```
class Car:
    pass
```
`pass` statement is used to indicate that this class is empty.

## The __init__() Method
__init__() is the special method that initializes an individual object. This method runs automatically each time an object of a class is created.

The __init__() method is generally used to perform operations that are necessary before the object is created.
- When you define __init__() in a class definition, its first parameter should be self.
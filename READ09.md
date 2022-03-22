
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example _init_ or _str_. These "dunders" or "special methods" in Python are also sometimes called "magic methods". But using this terminology can make them seem more complicated than they really are. You should treat these methods like a normal language feature.\
Languages such as Java and C# use the new operator to create a new instance of a class. In Python the _new() magic method is implicitly called before the __init_() method.\
Magic methods in Python are the special methods that start and end with the double underscores. They are also called dunder methods. Magic methods are not meant to be invoked directly by you, but the invocation happens internally from the class on a certain action. For example, when you add two numbers using the + operator, internally, the _add_() method will be called.\

Built-in classes in Python define many magic methods. Use the dir() function to see the number of magic methods inherited by a class. For example, the following lists all the attributes and methods defined in the int class.\
_str_() method
Another useful magic method is _str(). It is overridden to return a printable string representation of any user defined class. We have seen str() built-in function which returns a string from the object parameter. For example, str(12) returns '12'. When invoked, it calls the __str_() method in the int class.\
```
class Employee:
    def _init_(self):
        self.name='Swati'
        self.salary=10000
    def _str_(self):
        return 'name='+self.name+' salary=$'+str(self.salary)
```

```
Initialization and Construction	Description
_new_(cls, other)	To get called in an object's instantiation.
_init(self, other)	To get called by the __new_ method.
_del_(self)	Destructor method.
```
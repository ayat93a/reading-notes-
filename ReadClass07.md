# The Global Scope
From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution. The namespace of this module is the main global scope of your program.\
Whenever you run a Python program or an interactive session like in the above code, the interpreter executes the code in the module or script that serves as an entry point to your program. This module or script is loaded with the special name, __main__. From this point on, you can say that your main global scope is the scope of __main__.\
There’s only one global Python scope per program execution. This scope remains in existence until the program terminates and all its names are forgotten. Otherwise, the next time you were to run the program, the names would remember their values from the previous run.

You can access or reference the value of any global name from any place in your code.\
You can access or reference the value of any global name from any place in your code. This includes functions and classes. Here’s an example that clarifies these points:

```
>>> var = 100
>>> def func():
...     return var  # You can access var from inside func()
...
>>> func()
100
>>> var  # Remains unchanged
100

```
Inside func(), you can freely access or reference the value of var. This has no effect on your global name var, but it shows you that var can be freely accessed from within func(). On the other hand, you can’t assign global names inside functions unless you explicitly declare them as global names using a global statement, which you’ll see later on.\
Whenever you assign a value to a name in Python, one of two things can happen:

- You create a new name
- You update an existing name
The concrete behavior will depend on the Python scope in which you’re assigning the name. If you try to assign a value to a global name inside a function, then you’ll be creating that name in the function’s local scope, shadowing or overriding the global name. This means that you won’t be able to change most variables that have been defined outside the function from within the function.\
If you follow this logic, then you’ll realize that the following code won’t work as you might expect:
```
>>> var = 100  # A global variable
>>> def increment():
...     var = var + 1  # Try to update a global variable
...
>>> increment()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    increment()
  File "<stdin>", line 2, in increment
    var = var + 1
UnboundLocalError: local variable 'var' referenced before assignment
```
Within increment(), you try to increment the global variable, var. Since var isn’t declared global inside increment(), Python creates a new local variable with the same name, var, inside the function. In the process, Python realizes that you’re trying to use the local var before its first assignment (var + 1), so it raises an UnboundLocalError.\
You likely expect to be able to print the global var and be able to update var later, but again you get an UnboundLocalError. What happens here is that when you run the body of func(), Python decides that var is a local variable because it’s assigned within the function scope. This isn’t a bug, but a design choice. Python assumes that names assigned in the body of a function are local to that function.\
```
Global names can be updated or modified from any place in your global Python scope. Beyond that, the global statement can be used to modify global names from almost any place in your code, as you’ll see in The global Statement.

Modifying global names is generally considered bad programming practice because it can lead to code that is:

Difficult to debug: Almost any statement in the program can change the value of a global name.
Hard to understand: You need to be aware of all the statements that access and modify global names.
Impossible to reuse: The code is dependent on global names that are specific to a concrete program.
Good programming practice recommends using local names rather than global names. Here are some tips:

- Write self-contained functions that rely on local names rather than global ones.
- Try to use unique objects names, no matter what scope you’re in.
- Avoid global name modifications throughout your programs.
- Avoid cross-module name modifications.
- Use global names as constants that don’t change during your program’s execution.

```
# The nonlocal Statement
Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope. The following example shows how you can use nonlocal to modify a variable defined in the enclosing or nonlocal scope:
```
>>> def func():
...     var = 100  # A nonlocal variable
...     def nested():
...         nonlocal var  # Declare var as nonlocal
...         var += 100
...
...     nested()
...     print(var)
...
>>> func()
200
```
With the statement nonlocal var, you tell Python that you’ll be modifying var inside nested(). Then, you increment var using an augmented assignment operation. This change is reflected in the nonlocal name var, which now has a value of 200.

Unlike global, you can’t use nonlocal outside of a nested or enclosed function. To be more precise, you can’t use a nonlocal statement in either the global scope or in a local scope. Here’s an example:
```
>>> nonlocal my_var  # Try to use nonlocal in the global scope
  File "<stdin>", line 1
SyntaxError: nonlocal declaration not allowed at module level
>>> def func():
...     nonlocal var  # Try to use nonlocal in a local scope
...     print(var)
...
  File "<stdin>", line 2
SyntaxError: no binding for nonlocal 'var' found

```

Here, you first try to use a nonlocal statement in the global Python scope. Since nonlocal only works inside an inner or nested function, you get a SyntaxError telling you that you can’t use nonlocal in a module scope. Notice that nonlocal doesn’t work inside a local scope either.
# `if __name__ == __main__`

Before executing code, Python interpreter reads source file and define few special variables/global variables. --> `__name__` is one of these variables.

## *Python files are called modules* --> A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended. 

--> When the Python interpreter reads a source file, it executes all of the code found in it.\
--> befor executing the code,it sets the special  `__name__` variable to have a value `__main__`. If this file is being imported from another module, `__name__ ` will be set to the module’s name. Module’s name is available as value to `__name__ ` global variable. \
--> One reason for doing this is that sometimes you write a module (a .py file) where it can be executed directly. Alternatively, it can also be imported and used in another module. By doing the main check, you can have that code only execute when you want to run the module as a program and not have it execute when someone just wants to import your module and call your functions themselves.
___
# ASAC 
`__main__` is the name of the scope in which top-level code executes. A module’s `__name__` is set equal to ` __main__` when read from standard input, a script, or from an interactive prompt.

A module can discover whether or not it is running in the main scope by checking its own `__name__`, which allows a common idiom for conditionally executing code in a module when it is run as a script or with python -m but not when it is imported:

>if __name__ == "__main__":\
>     # execute only if run as a script \
>    main()  

For a package, the same effect can be achieved by including a __main__.py module, the contents of which will be executed when the module is run with -m.
___
# in my words :
if i have 2 moduls : *first.py* and *secound.py* \
if i import the secound.py into the first.py --> the interpture will excute for me all the code/ program from the secound into first \
if i use `if __name__ = __main__` in *first.py*--> Only the functions that i call it in the first.py will be excute.
___

Referances : 
- [Corey Schafer](https://www.youtube.com/watch?v=sugvnHA7ElY)
- [tutorialspoint `Code`](https://www.tutorialspoint.com/What-does-the-if-name-main-do-in-Python)


[Back to main](./README.md)
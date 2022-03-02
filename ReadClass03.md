# Exceptions 
1. occur when something goes wrong, due to incorrect code or input. When an exception occurs, the program immediately stops.
2. Different exceptions are raised for different reasons.
Common exceptions:
- ImportError: an import fails;
- IndexError: a list is indexed with an out-of-range number;
- NameError: an unknown variable is used;
- SyntaxError: the code can't be parsed properly;
- TypeError: a function is called on a value of an inappropriate type;
- ValueError: a function is called on a value of the correct type, but with an inappropriate value.
3. To handle exceptions, and to call code when an exception occurs, you can use a try/except statement.
The try block contains code that might throw an exception. If that exception occurs, the code in the try block stops being executed, and the code in the except block is run. If no error occurs, the code in the except block doesn't run.
4. A try statement can have multiple different except blocks to handle different exceptions.
Multiple exceptions can also be put into a single except block using parentheses, to have the except block handle all of them.
5. An except statement without any exception specified will catch all errors. These should be used sparingly, as they can catch unexpected errors and hide programming mistakes.
6. To ensure some code runs no matter what errors occur, you can use a finally statement. The finally statement is placed at the bottom of a try/except statement. Code within a finally statement always runs after execution of the code in the try, and possibly in the except
___
 # File Mauipulate 
1. Opening Files ==> open function.
- specify the mode used to open a file by applying a second argument to the open function.
- Sending "r" means open in read mode, which is the default.
- Sending "w" means write mode, for rewriting the contents of a file.
- Sending "a" means append mode, for adding new content to the end of the file.
- Adding "b" to a mode opens it in binary mode, which is used for non-text files (such as image and sound files).
2. Once a file has been opened and used, you should close it.
This is done with the close method of the file object.
 
 
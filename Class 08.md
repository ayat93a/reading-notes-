# List Comprehensions in Python
## Syntax -->
 my_new_list = `newList = [ expression(element) for element in oldList if condition ] `\
 --> you’re going to perform an expression on each item in the list. The expression will determine what item is eventually stored in the output list.\
 the three ingredients are necessary for a python list comprehension to work.
- First is the expression we’d like to carry out. expression inside the square brackets.
- Second is the object that the expression will work on. item inside the square brackets.
- Finally, we need an iterable list of objects to build our new list from. list inside the square brackets.\
Not only can you perform expressions on an entire list in a single line of code, but, as we’ll see later, it’s possible to add conditional statements in the form of filters, which allows for more precision in the way lists are handled.\
### Advantages of List Comprehension
- More time-efficient and space-efficient than loops.
- Require fewer lines of code.
- Transforms iterative statement into a formula.
### Notes about Lists Comprehensions
1- List comprehension methods are an elegant way to create and manage lists.\
2- In Python, list comprehensions are a more compact way of creating lists.\  
3- More flexible than for loops, list comprehension is usually faster than other methods.\ 

## Create a List Using Loops and List Comprehension in Python
### List Comprehensions vs For Loop
``` 
# Empty list
List = []

# Traditional approach of iterating
for character in 'Geeks 4 Geeks!':
	List.append(character)

# Display list
print(List)

```
Above is the implementation of the traditional approach to iterate through a list, string, tuple, etc. Now list comprehension does the same task and also makes the program more simple.

List Comprehensions translate the traditional iteration approach using for loop into a simple formula hence making them easy to use. Below is the approach to iterate through a list, string, tuple, etc. using list comprehension.
```
# Using list comprehension to iterate through loop
List = [character for character in 'Geeks 4 Geeks!']

# Displaying list
print(List)

```

The list comprehensions are more efficient both computationally and in terms of coding space and time than a for loop. Typically, they are written in a single line of code. The below program depicts the difference between for loops and list comprehension based on performance.
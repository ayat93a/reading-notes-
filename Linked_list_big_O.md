# Pain and Suffering
With No Pain there is No Gain. 
Pain is nessecary for big dream, suffer is just suffer.
I have 10 weeks to can achive my gole in being a *WEB DEVELOPER* and can complete my first project in *Artificial Intelligence*

# Beginners Guide to Big O

## What big O notation is

Big O notation is a symbology used to express the asymptotic behavior of functions in complexity theory, computer science, and mathematics. It essentially shows you how quickly a function increases or diminishes, The letter `O` is used because the rate of growth of a
function is also called its order.
### Illistraion example 
when analyzing some algorithm, one might find that the time (or the
number of steps) it takes to complete a problem of size n is given by [T(n) = 4 n ^2 - 2 n + 2].
If we ignore constants (which makes sense because those depend on the particular
hardware the program is run on ~ We can say that its the number of console.log that will excute for the same algorithem as mentioned in ref #2 **~) and slower growing terms, we could say `T(n) grows at the order of n^2  and write:T(n) = O(n^2). ==> this example from ref#3.

**There are no constants or low-order terms in the big-O expressions. This is because constants and low-order terms don't matter when N is high enough (a constant-time method will be quicker than a linear-time approach, which will be faster than a quadratic-time algorithm).
For a problem of size N:
- a constant-time algorithm is "order 1": O(1)
- a linear-time algorithm is "order N": O(N)
- a quadratic-time algorithm is "order N squared": O(N^2)

## Why O notation 

What is the efficiency of an algorithm or a line of code? Efficiency encompasses a wide range of resources, including: 
-  CPU (processing) time 
-  memory utilization
-  disk usage 
- network usage.
All are significant, but we'll focus on time complexity (CPU usage).
The Performance is measured by how much time/memory/disk/... is actually used when a program is run. This depends on the machine, compiler, etc. as well as the code Complexity.
Complexity mainly mean what happens as the size of the problem being solved gets larger? and that what the reason for why the big O notation are measured.


## How to calculate big O notation
*We express complexity using big-O notation.* ; Big O is a term that indicates the worst-case scenario and may be used to describe the amount of time an algorithm takes to execute or the amount of space it takes up (in memory or on disk).

The following is the general step-by-step process for Big-O runtime analysis:#Ref 4
- Figure out what the input is and what n represents.
- Express the maximum number of operations, the algorithm performs in terms of n.
- Eliminate all excluding the highest order terms.
- Remove all the constant factors. 
*For any algorithm, the Big-O analysis should be straightforward as long as we correctly identify the operations that are dependent on n, the input size.*
### Runtime Analysis of Algorithms 
In most cases, we performed performance analysis to assess and evaluate the worst-case theoretical running time complexities of algorithms.
Any algorithm's quickest feasible running time is O(1), also known as Constant Running Time. In this situation, regardless of the quantity of the input, the algorithm takes the same amount of time to run. This is the optimal algorithm runtime, however it is seldom achieved.
In practice, an algorithm's performance (Runtime) is determined by n, which refers to the amount of the input or the number of operations necessary for each input item.
From best to worst performance (Running Time Complexity), the algorithms are categorised as follows:
___
![](./readindC01/Capture.PNG)

Where, n is the input size and c is a positive constant. 
___
![](./readindC01/Capture2.PNG)

## Mathematical Examples of Runtime Analysis: 

![](./readindC01/Capture0.PNG)



___
#### Referances
1. [Programming with Mosh](https://www.youtube.com/watch?v=BBpAmxU_NQo)
2. [Web Dev Simplified](https://www.youtube.com/watch?v=itn09C2ZB9Y&t=72s)
3. [MIT Big Notation Lecture](http://web.mit.edu/16.070/www/lecture/big_o.pdf)
4. [geeksforgeeks](https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)


# Linked List
Linked lists are a common alternative to arrays in the implementation of
data structures. Each item in a linked list contains a data element of some
type and a pointer to the next item in the list. It is easy to insert and delete
elements in a linked list, which are not natural operations on arrays, since
arrays have a fixed size. On the other hand access to an element in the
middle of the list is usually O(n), where n is the length of the list.
An item in a linked list consists of a struct containing the data element
and a pointer to another linked list. In C0 we have to commit to the type
of element that is stored in the linked list. We will refer to this data as
having type elem, with the expectation that there will be a type definition
elsewhere telling C0 what elem is supposed to be. Keeping this in mind
ensures that none of the code actually depends on what type is chosen.
These considerations give rise to the following definition:
```
struct list_node {
elem data;
struct list_node* next;
};
typedef struct list_node list;
```
This definition is an example of a recursive type. A struct of this type
contains a pointer to another struct of the same type, and so on. We usually
use the special element of type t*, namely NULL, to indicate that we have
reached the end of the list. Sometimes (as will be the case for our use of
linked lists in stacks and queues), we can avoid the explicit use of NULL and
obtain more elegant code. The type definition is there to create the type
name list, which stands for struct list_node, so that a pointer to a list
node will be list*.
There are some restriction on recursive types. For example, a declaration such as
```
struct infinite {
int x;
struct infinite next;
}
```
would be rejected by the C0 compiler because it would require an infinite
amount of space. The general rule is that a struct can be recursive, but
the recursion must occur beneath a pointer or array type, whose values are
addresses. This allows a finite representation for values of the struct type.
We don’t introduce any general operations on lists; let’s wait and see
what we need where they are used. Linked lists as we use them here are
a concrete type which means we do not construct an interface and a layer of
abstraction around them. When we use them we know about and exploit
their precise internal structure. This is contrast to abstract types such as
queues or stacks (see next lecture) whose implementation is hidden behind
an interface, exporting only certain operations. This limits what clients
can do, but it allows the author of a library to improve its implementation
without having to worry about breaking client code. Concrete types are
cast into concrete once and for all.
List segments
A lot of the operations we’ll perform in the next few lectures are on segments
of lists: a series of nodes starting at start and ending at end.
![](./Capture1.PNG)
This is the familiar structure of an “inclusive-lower, exclusive-upper” bound:
we want to talk about the data in a series of nodes, ignoring the data in
the last node. That means that, for any non-NULL list node pointer l, a
segment from l to l is empty (contains no data). Consider the following
structure:
![](./Capture2.PNG)
According to our definition of segments, the data in the segment from a1 to
a4 is the sequence 3, 7, 3, the data in the segment from a2 to a3 contains the
sequence 7, and the data in the segment from a1 to a1 is the empty sequence.
Note that if we compare the pointers a1 and a3 C0 will tell us they are not
equal – even though they contain the same data they are different locations
in memory.


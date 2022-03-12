# How to use the Random Module in Python
The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.\
We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck or when making your password database more secure or powering a random page feature of your website.

# Random functions
The Random module contains some very useful functions.

## Randint
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number.
```
import random
print random.randint(0, 5)
>>> This will output either 1, 2, 3, 4 or 5.
```
## Random
If you want a larger number, you can multiply it.
```
import random
random.random() * 100
```
### Choice
Generate a random value from the sequence
```
random.choice( ['red', 'black', 'green'] ).
```
the choice function can often be used for choosing a random element from a list.
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```
## Shuffle
The shuffle function, shuffles the elements in list in place, so they are in a random order.

```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
>>> Output:
# print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
# of course your results will vary
```

## Randrange
Generate a randomly selected element from range(start, stop, step)
```
random.randrange(start, stop[, step])
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```

# What is Risk Analysis in Software Testing and how to perform it?
risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.\
In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks.\
When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.\
what could be the possible risks that you could encounter?\
- Use of new hardware
- Use of new technology
- Use of new automation tool
- The sequence of code
- Availability of test resources for the application\
now must know there are certain risks that are unavoidable.am enumerating them below:

- The time that you allocated for testing

- A defect leakage due to the complexity or size of the application

- Urgency from the clients to deliver the project

- Incomplete requirements\
In such cases, you have to tackle the situation with care. Following points can be taken care of:

- Conduct Risk Assessment review meeting

- Use maximum resources to work on high-risk areas

- Create a Risk Assessment database for future use

- Identify and notice the risk magnitude indicators: high, medium, low.\
## Risk Identification
There are different sets of risks included in the risk identification process. Those are as follows:

- Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

- Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

- Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

- Software Risks: You should be well versed with the risks associated with the software development process.

## The perspective of Risk Assessment
There are three perspectives of Risk Assessment:

- Effect

- Cause

- Likelihood

- Effect – To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.

- Cause – To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.

- Likelihood – To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.

Now, heading forward, the question that would be hovering over your mind is, how actually shall we perform risk analysis? Well, here is your solution!

## How to perform Risk Analysis?
There are three steps:\

- Searching the risk

- Analyzing the impact of each individual risk

- Measures for the risk identified

# TestCoverage

Test coverage is a useful tool for finding untested parts of a codebase. Test coverage is of little use as a numeric statement of how good your tests are.\
If you make a certain level of coverage a target, people will try to attain it. The trouble is that high coverage numbers are too easy to reach with low quality testing. At the most absurd level you have AssertionFreeTesting. But even without that you get lots of tests looking for things that rarely go wrong distracting you from testing the things that really matter.\
Like most aspects of programming, testing requires thoughtfulness. TDD is a very useful, but certainly not sufficient, tool to help you get good tests. If you are testing thoughtfully and well, I would expect a coverage percentage in the upper 80s or 90s. I would be suspicious of anything like 100% - it would smell of someone writing tests to make the coverage numbers happy, but not thinking about what they are doing.\
The reason, of course, why people focus on coverage numbers is because they want to know if they are testing enough. Certainly low coverage numbers, say below half, are a sign of trouble. But high numbers don't necessarily mean much, and lead to ignorance-promoting dashboards. Sufficiency of testing is much more complicated attribute than coverage can answer. I would say you are doing enough testing if the following is true:
- You rarely get bugs that escape into production, and
- You are rarely hesitant to change some code for fear it will cause production bugs.

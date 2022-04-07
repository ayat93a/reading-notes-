# How To Run Linear Regressions In Python Scikit-Learn

*Scikit-learn is a Python package that simplifies the implementation of a wide range of Machine Learning (ML) methods for predictive data analysis, including linear regression.*

- Linear regression can be thought of as finding the straight line that best fits a set of scattered data points , You can then project that line to predict new data points. Linear regression is a fundamental ML algorithm due to its comparatively simple and core properties.

## Linear Regression Concepts
A basic understanding of statistical math is key to comprehending linear regression, as is a good grounding in ML concepts.


### The following are some key concepts you will come across when you work with scikit-learn’s linear regression method:
- Best Fit – the straight line in a plot that minimizes the deviation between related scattered data points.
- Coefficient – also known as a parameter, is the factor a variable is multiplied by. In linear regression, a coefficient represents changes in a Response Variable (see below).
- Coefficient of Determination – the correlation coefficient denoted as 𝑅². Used to describe the precision or degree of fit in a regression. 
- Correlation – the relationship between two variables in terms of quantifiable strength and degree, often referred to as the ‘degree of correlation’.  Values range between -1.0 and 1.0. 
- Dependent Feature – a variable denoted as y in the slope equation y=ax+b. Also known as an Output, or a Response. 
- Estimated Regression Line – the straight line that best fits a set of scattered data points.
- Independent Feature – a variable denoted as x in the slope equation y=ax+b. Also known as an Input, or a predictor. 
- Intercept – the location where the Slope intercepts the Y-axis denoted b in the slope equation y=ax+b. 
- Least Squares – a method of estimating a Best Fit to data, by minimizing the sum of the squares of the differences between observed and estimated values.
- Mean – an average of a set of numbers, but in linear regression, Mean is modeled by a linear function.
- Ordinary Least Squares Regression (OLS) – more commonly known as Linear Regression. 
- Residual – vertical distance between a data point and the line of regression (see Residual in Figure 1 below).
- Regression – estimate of predictive change in a variable in relation to changes in other variables (see Predicted Response in Figure 1 below).
- Regression Model – the ideal formula for approximating a regression.
- Response Variables – includes both the Predicted Response (the value predicted by the regression) and the Actual Response, which is the actual value of the data point (see Figure 1 below).
- Slope – the steepness of a line of regression. Slope and Intercept can be used to define the linear relationship between two variables: y=ax+b.
- Simple Linear Regression – a linear regression that has a single independent variable.

### Linear Regression Class Definition
```
from sklearn.linear_model import LinearRegression
sklearn.linear_model.LinearRegression()
```

### How to Create a Linear Regression Model
In this example, a linear regression model is created based on data in a numpy array.  :
```
# Import the packages and classes needed in this example:
import numpy as np
from sklearn.linear_model import LinearRegression

# Create a numpy array of data:
x = np.array([6, 16, 26, 36, 46, 56]).reshape((-1, 1))
y = np.array([4, 23, 10, 12, 22, 35])

# Create an instance of a linear regression model and fit it to the data with the fit() function:
model = LinearRegression().fit(x, y) 

# The following section will get results by interpreting the created instance: 

# Obtain the coefficient of determination by calling the model with the score() function, then print the coefficient:
r_sq = model.score(x, y)
print('coefficient of determination:', r_sq)

# Print the Intercept:
print('intercept:', model.intercept_)

# Print the Slope:
print('slope:', model.coef_) 

# Predict a Response and print it:
y_pred = model.predict(x)
print('Predicted response:', y_pred, sep='\n')

```

Data visualization is the graphic representation of data. It involves producing images that communicate relationships among the represented data to viewers.

Visualizing data is an essential part of data analysis and machine learning. We'll use Python libraries Matplotlib  to learn and apply some popular data visualization techniques. We'll use the words chart, plot, and graph interchangeably in this tutorial.

To begin, let's install and import the libraries. We'll use the matplotlib.pyplot module for basic plots like line and bar charts. It is often imported with the alias plt. We'll use the seaborn module for more advanced plots. It is commonly imported with the alias sns.

!pip install matplotlib seaborn --upgrade --quiet

import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
Notice this we also include the special command %matplotlib inline to ensure that our plots are shown and embedded within the Jupyter notebook itself. Without this command, sometimes plots may show up in pop-up windows.

 

How to Create a Line Chart in Python
The line chart is one of the simplest and most widely used data visualization techniques. A line chart displays information as a series of data points or markers connected by straight lines.

You can customize the shape, size, color, and other aesthetic elements of the lines and markers for better visual clarity.

Here's a Python list showing the yield of apples (tons per hectare) over six years in an imaginary country called Kanto.

yield_apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931]
We can visualize how the yield of apples changes over time using a line chart. To draw a line chart, we can use the plt.plot function.

plt.plot(yield_apples)
image-145
Calling the plt.plot function draws the line chart as expected. It also returns a list of plots drawn [<matplotlib.lines.Line2D at 0x7ff70aa20760>], shown within the output. We can include a semicolon (;) at the end of the last statement in the cell to avoiding showing the output and display just the graph.

plt.plot(yield_apples);
image-146
Let's enhance this plot step-by-step to make it more informative and beautiful.

How to Customize the X-axis in MatPlotLib
The X-axis of the plot currently shows list element indices 0 to 5. The plot would be more informative if we could display the year for which we're plotting the data. We can do this by two arguments plt.plot.

years = [2010, 2011, 2012, 2013, 2014, 2015]
yield_apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931]

plt.plot(years, yield_apples)
image-147
Axis Labels in MatPlotLib
We can add labels to the axes to show what each axis represents using the plt.xlabel and plt.ylabel methods.

plt.plot(years, yield_apples)
plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)');
image-148
How to Plot Multiple Lines in MatPlotLib
You can invoke the plt.plot function once for each line to plot multiple lines in the same graph. Let's compare the yields of apples vs. oranges in Kanto.

years = range(2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.plot(years, apples)
plt.plot(years, oranges)
plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)');
image-149
Chart Title and Legend in MatPlotLib
To differentiate between multiple lines, we can include a legend within the graph using the plt.legend function. We can also set a title for the chart using the plt.title function.

plt.plot(years, apples)
plt.plot(years, oranges)

plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')

plt.title("Crop Yields in Kanto")
plt.legend(['Apples', 'Oranges']);
image-150
How to Use Line Markers in MatPlotLib
We can also show markers for the data points on each line using the marker argument of plt.plot.

Matplotlib provides many different markers like a circle, cross, square, diamond, and more. You can find the full list of marker types here: https://matplotlib.org/3.1.1/api/markers_api.html (Links to an external site.) .

plt.plot(years, apples, marker='o')
plt.plot(years, oranges, marker='x')

plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')

plt.title("Crop Yields in Kanto")
plt.legend(['Apples', 'Oranges']);
image-151
How to Style Lines and Markers in MatPlotLib
The plt.plot function supports many arguments for styling lines and markers:

color or c – Set the color of the line (supported colors (Links to an external site.))
linestyle or ls – Choose between a solid or dashed line
linewidth or lw – Set the width of a line
markersize or ms – Set the size of markers
markeredgecolor or mec – Set the edge color for markers
markeredgewidth or mew – Set the edge width for markers
markerfacecolor or mfc – Set the fill color for markers
alpha – Opacity of the plot
Check out the documentation for plt.plot to learn more: https://matplotlib.org/api/_as_gen/matplotlib.pyplot.plot.html#matplotlib.pyplot.plot (Links to an external site.) .

plt.plot(years, apples, marker='s', c='b', ls='-', lw=2, ms=8, mew=2, mec='navy')
plt.plot(years, oranges, marker='o', c='r', ls='--', lw=3, ms=10, alpha=.5)

plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')

plt.title("Crop Yields in Kanto")
plt.legend(['Apples', 'Oranges']);
image-152
The fmt argument provides a shorthand for specifying the marker shape, line style, and line color. You can provide it as the third argument to plt.plot.

fmt = '[marker][line][color]'

plt.plot(years, apples, 's-b')
plt.plot(years, oranges, 'o--r')

plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')

plt.title("Crop Yields in Kanto")
plt.legend(['Apples', 'Oranges']);
image-153
You can use the plt.figure function to change the size of the figure.

plt.plot(years, oranges, 'or')
plt.title("Yield of Oranges (tons per hectare)");
image-154
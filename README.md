# Task-2

# Importing necessary libraries
import matplotlib.pyplot as plt
import numpy as np

# Coefficients for the quadratic equation: ax^2 + bx + c
a = 0.5
b = 2
c = 1

# Define the weather model equation
def weather_model(x):
    return a * x**2 + b * x + c

# Generate x values using NumPy linspace
x_values = np.linspace(-10, 10, 100)  

# Calculate corresponding y values using the weather_model function
y_values = weather_model(x_values)

# Plotting the weather model
plt.plot(x_values, y_values, label='Weather Model')

# Adding labels and title to the plot
plt.title('Weather Model')
plt.xlabel('Time')
plt.ylabel('Temperature')

# Displaying the legend
plt.legend()

Keyboard input
Code:
import numpy as np
import matplotlib.pyplot as plt
def weather_model(x, a, b, c):
    return a*x**2 + b*x + c #equation
a = float(input("Enter the value of a: "))#enter the a value 
b = float(input("Enter the value of b: "))#enter the b value 
c = float(input("Enter the value of c: "))#enter the c value 

x_values = np.linspace(-10, 10, 400)#creates a list of 400 values from x axis of -10 to 10
y_values = weather_model(x_values, a, b, c)
x_specific = float(input("Enter the specific value of x: "))# enter the specific x value
y_specific = weather_model(x_specific, a, b, c)
plt.figure(figsize=(10, 6))
plt.plot(x_values, y_values, label=f'{a}x^2 + {b}x + {c}')   
plt.plot([x_specific], [y_specific], 'ro')  #ro means r-red o-circle 
plt.title('Weather Model') #plot the title
plt.xlabel('Time')
plt.ylabel('Temperature')
plt.legend()
plt.grid(True)
plt.show()

# Displaying the grid on the plot
plt.grid(True)

# Showing the plot
plt.show()

#Read from a file
# Importing necessary libraries
import numpy as np
import matplotlib.pyplot as plt

# Define the quadratic function
def weather_model(x, a, b, c):
    return a * np.power(x, 2) + b * x + c

# Load parameters from the 'parameters.txt' file
parameters = np.loadtxt('parameters.txt')

# Generate x values using NumPy linspace
x_values = np.linspace(-10, 10, 400)

# Create a figure for the plot
plt.figure(figsize=(10, 6))

# Loop through each row in the parameters array
for test in parameters:
    # Extract values for x, a, b, c from the current row
    x, a, b, c = test

    # Calculate y values for the entire range of x values
    y_values = weather_model(x_values, a, b, c)

    # Plot the quadratic function for the entire range
    plt.plot(x_values, y_values, label=f'{a}x^2 + {b}x + {c}')

# Adding labels and title to the plot
plt.title('Quadratic Functions')
plt.xlabel('x')
plt.ylabel('y')

# Displaying the legend
plt.legend()

# Displaying the grid on the plot
plt.grid(True)

# Showing the plot
plt.show()

#Single set of input
import matplotlib.pyplot as plt
import numpy as np

def weather_model(x, a, b, c):
    return a * x**2 + b * x + c

# Read parameters from the file
with open('parameters.txt', 'r') as f:
    line = f.readline()
    x_specific, a_specific, b_specific, c_specific = map(float, line.split())

# Generate x values using NumPy linspace
x_values = np.linspace(-10, 10, 400)

# Calculate y values for the entire range of x values
y_values = weather_model(x_values, a_specific, b_specific, c_specific)

# Calculate y values for a specific x value
y_specific = weather_model(x_specific, a_specific, b_specific, c_specific)

# Plotting the weather model for the entire range
plt.figure(figsize=(10, 6))
plt.plot(x_values, y_values, label=f'{a_specific}x^2 + {b_specific}x + {c_specific}')

# Plotting the specific point in red
plt.plot(x_specific, y_specific, 'ro', label=f'Specific Point ({x_specific}, {y_specific})')

# Adding labels and title to the plot
plt.title('Quadratic Function')
plt.xlabel('x')
plt.ylabel('y')

# Displaying the legend
plt.legend()

# Displaying the grid on the plot
plt.grid(True)

# Showing the plot
plt.show()

#Multiset of input:
# Importing necessary libraries
import matplotlib.pyplot as plt
import numpy as np

# Define the quadratic function
def weather_model(x, a, b, c):
    return a * x**2 + b * x + c

# Read parameters from the file
with open('parameters.txt', 'r') as f:
    lines = f.readlines()

# Generate x values using NumPy linspace
x_values = np.linspace(-10, 10, 400)

# Create a figure for the plot
plt.figure(figsize=(10, 6))

# Loop through each line in the file to extract parameters
for line in lines:
    x_specific, a, b, c = map(float, line.split())

    # Calculate y values for the entire range of x values
    y_values = weather_model(x_values, a, b, c)

    # Calculate y value for the specific x value
    y_specific = weather_model(x_specific, a, b, c)

    # Plot the quadratic function for the entire range
    plt.plot(x_values, y_values, label=f'{a}x^2 + {b}x + {c}')

    # Plot the specific point in red
    plt.plot(x_specific, y_specific, 'ro')

# Adding labels and title to the plot
plt.title('Quadratic Functions')
plt.xlabel('x')
plt.ylabel('y')

# Displaying the legend
plt.legend()

# Displaying the grid on the plot
plt.grid(True)

# Showing the plot
plt.show()



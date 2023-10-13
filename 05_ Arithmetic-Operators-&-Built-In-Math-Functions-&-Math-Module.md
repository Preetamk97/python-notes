```py
# Importing the 'math' module 
import math


# Arithmetic Operators
#*******************************************************************************************************

age = 50

# age = age + 1     # Addition
# age += 1

# age = age - 1     # Subtraction
# age -= 1

# age = age * 2     # Multiplication
# age *= 2

# age = age / 2     # Division : returns the quotient
# age /= 2

# age = age % 2     # Modulus : returns the remainder
# age %= 2

# age = age ** 2    # Exponent/Power
# age **= 2

print(age)




# Some Built-In Math Functions
#**************************************************************************************************************

x = 3.14
y = -4
z = 5

# result = round(x)     # 3    # rounds up to nearest integer
# result = abs(y)       # 4   # returns the positive value
# result = pow(2, 3)    # 8     # power(base, index)
# result = max(x, y, z)   # 5     # returns the maximum value among x, y, and z variables
result = min(x, y, z)   # -4     # returns the minimum value among x, y, and z variables

print(result)


# round(x, y)
# -----------
x = 3.141592653589793
x = round(x, 3)    # round x to 3 decimal places
print(x)
# 3.142



# Math Module:
#***************************************************************************************************************

print(math.e)  
# 2.718281828459045
# The number e, also known as Euler's number, is a mathematical constant approximately equal to 2.71828 
# We can use this constant value in our code using 'math' module.

print(math.pi)
# 3.141592653589793
# 'math' module also provides the constant value of pi (= 3.14159265359)

# Finding the square-root of a number
x = 9
print(math.sqrt(9))
# 3.0


# .ceil() = returns the next greatest integer
x = 9.7
print(math.ceil(x))  # 10

# floor() = returns the previous greatest integer
x = 9.7
print(math.floor(x))    # 9


# Program to find the Area of a Circle (Using 'math' module)
#------------------------------------------------------------

# taking input 'radius' and typecasting it to 'float' datatype
radius = float(input("Enter radius of the circle: "))  # 10.5

# area of circle = (pi)(r**2)
area = math.pi * math.pow(radius, 2)

#  printing the 'area' as it is
print(f"Area of your circle is : {area}cm^2")  
# Area of your circle is : 346.3605900582747cm^2

# rounding the 'area' value to 2 decimal places while printing
print(f"Area of your circle is : {round(area, 2)}cm^2") 
# Area of your circle is : 346.36cm^2
```
- **Module** is a file containing some code that you want to include in your program.
- We use `import` statement to include **modules** (***built-in*** or ***self-created***) into our program.
- Useful to break up a large program into ***reusable separate files***. 

# Are all built-in Python Modules written in Python language itself?

No, not all built-in Python modules are written in Python language itself. While many built-in modules are implemented in Python, some modules are implemented in C or other programming languages for performance or to interact with low-level system resources.

# Ways of Importing a Module:

```py
import math

import math as m        # You can give your module a nickname inside the programe, especilaly if the 
                        # module name is too long.
                        
from math import pi     # impoting "math.pi" directly
```


# Creating our own Module:


- Create 2 **.py** files - **play.py** & **exampleModule.py**

## **exampleModule.py**

```py
pi = 3.14159

def square(x):
   return x ** 2

def cube(x):
   return x ** 3

def circumference(radius):
   return 2 * pi * radius

def area(radius):
   return pi * radius ** 2
```

## **play.py**

```py
import exampleModule

result = exampleModule.pi
print(result)
# 3.14159

result = exampleModule.square(3)
print(result)
# 9

result = exampleModule.cube(3)
print(result)
# 27

result = exampleModule.circumference(3)
print(result)
# 18.849539999999998

result = exampleModule.area(3)
print(result)
# 28.27431
```
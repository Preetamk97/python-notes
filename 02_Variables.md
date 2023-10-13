```py
# Variable = A reusable container for storing a value. A variable behaves as if it were the value it contains.

# Declaring and Initializing a Variable
#**************************************
age = 16


# String Concatenation : Printing a 'variable value' along with "String" value using print()
#*******************************************************************************************

# Way 1:
#-------
print("You are " + str(age) + " years old.") 
# Since 'age = 16' is an integer value, we need to typecast it to 'string' datatype using 'str()' function before concatenating it along with "String" values inside print().
# You are 16 years old.

# Way 2:
#-------
print("You are",str(age),"years old.") 
# Comma(,) adds a whitespace in the printed line automatically. No need to give extra spaces inside the string.
# You are 16 years old.


# Note:
#------
# print("You are " + age + " years old.") 
# The above line of code will give a TypeError 


# Way 3: Using f-String
#----------------------
print(f"You are {age} years old.")
# You are 16 years old.


# Basic Datatypes in Python
#***************************

players = 11  # Integer

gpa = 3.2  # Float

name = "pritam" # String

for_Sale = True  # Boolean


# Tips and Tricks
#****************

# Trick 1:
#----------
x, y, z = 1, 2, 3

print(x)  # 1
print(y)  # 2
print(z)  # 3


# Trick 2:
#---------
x = y = z = 27

print(x)  # 27
print(y)  # 27
print(z)  # 27
```
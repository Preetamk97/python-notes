```py
# type casting = The process of converting a value of one data type to another datatype
#                (string, integer, float, boolean)

# There are 2 types of typecasting basically - Implicit & Explicit.

name = "Bro"  # str
age = 21    # int
gpa = 1.9   # float
student = True  # bool


# Printing the Datatype of a Variable using type()
# ************************************************
print(type(name))
# <class 'str'>
print(type(age))
# <class 'int'>
print(type(gpa))
# <class 'float'>
print(type(student)) 
# <class 'bool'>)



# Explicit TypeCasting
# ****************************************************************************************************************

# age = 21    # int
# Typecasting 'int' type 'age' variable to 'float' datatype
age = float(age)
print(age) 
# 21.0


# gpa = 1.9     # float
# Typecasting 'float' type 'gpa' variable to 'int' datatype
gpa = int(gpa)
print(gpa) 
# 1

# student = True  # bool
# Typecasting 'bool' type 'student' variable to 'str' datatype
student = str(student)
print(type(student))
# <class 'str'>

# age = 21    # int
# Typecasting 'int' type 'age' variable to 'boolean' datatype
age = bool(age)
print(age)
# True
# Any integer/float other than zero (0), whether positive or negative, when typecasted to 'boolean' datatype always returns 'True'
# Only zero (0), when typecasted to 'boolean' datatype always returns 'False'.

# gpa = 1.9     # float
# Typecasting 'float' type 'gpa' variable to 'boolean' datatype
gpa = bool(gpa)
print(gpa) 
# True


gpa = 0
gpa = bool(gpa)
print(gpa)
# False


# name = "Bro"  # str
# # Typecasting 'str' type 'name' variable to 'boolean' datatype
name = bool(name)
print(name)
# True
# If the string is not an empty string, then typecasting it to boolean datatype will always return 'True'

name = ""  # Empty String
name = bool(name)
print(name)
# False

name = " "  # Non-Empty String contains single whitespace
name = bool(name)
print(name)
# True
# If the string is not an empty string, then typecasting it to boolean datatype will always return 'True'




# Implicit TypeCasting
# ****************************************************************************************************************

x = 2
y = 2.0

x = x/y     # (int/float)
print(x)
# 1.0  
# int/float = float
# int(x) is getting converted to float(x) implicitly.
# This action of implicitly converting a variable of one datatype to another is called Implicit Typecasting.
```
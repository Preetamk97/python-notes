```py
# User Input In Python

name = input("Enter Your Name : ")   # Bro
# Storing the input accepted from the user inside the 'name' variable.
print(f"Hello {name}")  
# Hello Bro

age = int(input("Enter your age: "))     # 26
# The default datatype of an User Input is 'String'. 
# But we can always "typecast" an User Input from its default 'String' datatype to any datatype as per our need.
# In the above line of code, we are "typecasting" the User Input Value of 'age' from 'str' to 'int' datatype, so that we can perform mathematical operations with/on the 'age' variable.
age = age + 1
print(f"You are {age} years old.")  
# You are 27 years old.
```
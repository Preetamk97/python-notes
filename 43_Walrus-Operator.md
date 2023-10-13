```py
# Walrus Operator --->  :=   
# New feature of Python 3.8
# Assignment Expression aka Walrus Operator
# Assigns values to variables as part of a larger expression

# Use Example 1:
#################

# happy = True    
# print(happy)    


print(happy := True)

# In the above line of code, we are executing both codes `happy = True` & 'print(happy)' ---> with just a single line of code  ---> using Walrus Operator.

# Use Example 2:
################

# foods = list()
# while True:
#   food = input("What food do you like?: ")
#       if food == "quit":
#           break
#   foods.append(food)

foods = list()
while food := input("What food do you like?: ") != "quit":
    foods.append(food)


#           food := input("What food do you like?: ") != "quit"

# In this expression, we are 
#                           1. taking an input & and assigning this input to 'food' variable
#                           2. and checking if this value of 'food' variable is NOT EQUAL to string "quit"
# all at the same time using Walrus Operator (:=).
```
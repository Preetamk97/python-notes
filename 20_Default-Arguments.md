```py
#  Default Argument = A default value for certain parameter.
#                     It is used when that argument is ommited while calling the function.
#                     Default arguments should always be added at the end of the parameters list - while defining   
#                     the function(parameters list,,)

# 4 TYPES OF ARGUMENTS IN PYTHON:  # POSITIONAL  (Last Lesson)
                                   # DEFAULT    (This Lesson)
                                   # KEYWORD    (Next Lesson)
                                   # ARBITRARY  (Some Future Lesson)

# ----- EXAMPLE 1 -----
def net_price(list_price, discount=0, tax=0.05):
   return list_price * (1 - discount) * (1 - tax)

print(net_price(500))           # 475.0     # discount=0, tax=0.05
print(net_price(500, 0.1))      # 427.5     # tax=0.05
print(net_price(500, 0.1, 0))   # 450.0     # all values provided


# ----- EXAMPLE 2 -----
import time

def count(end, start=0): 
    for x in range(start, end+1):   # 'end' value is exclusive in range(), so to include it, we add +1
        print(x)
        time.sleep(1)
    print("DONE!")

count(10)   # start=0  (by default)
count(30, 15)   # start=15
```
```py
# lambda function = function written in 1 line using 'lambda' keyword
#                   accepts any number of arguments, but only has one expression.
#                   (think of it as a shortcut)
#
# Syntax -- lambda parameters:expression

double = lambda x: x * 2
print(double(1))    # 2

multiply = lambda x, y: x * y
print(multiply(1,2))    # 2

add = lambda x, y, z: x + y + z
print(add(1,2,3))   # 6

full_name = lambda first_name, last_name: first_name+" "+last_name
print(full_name("Bro","Code"))      # "Bro Code"

age_check = lambda age: True if age >= 18 else False
print(age_check(18))        # True
```
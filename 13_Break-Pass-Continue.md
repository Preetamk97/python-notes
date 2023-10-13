# `break` Keyword:

```py
for x in range(1,21):  # x in range 1-20
    if(x==13):
        break   # As soon as x becomes =13, the program will break out of the entire for-loop
    else:
        print(x)
# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
# 11
# 12
```


# `continue` Keyword:

```py
for x in range(1,21):  # x in range 1-20
    if(x==13):
        continue    # For iteration x=13, skip the execution of rest of the for-loop code after 'continue'   
                    # keyword; and continue as usual from the next iteration
    else:
        print(x)
# 1
# 2 
# 3 
# 4 
# 5 
# 6 
# 7 
# 8 
# 9 
# 10
# 11
# 12
# 14
# 15
# 16
# 17
# 18
# 19
# 20
```


# `pass` Keyword:

The **pass** keyword is used as a ***placeholder*** for future code.

When the **pass** statement is executed, nothing happens, but you avoid getting an error when empty code is not allowed.

Empty code is not allowed in loops, function definitions, class definitions, or in if statements.

## Ex 1: Create a placeholder for future code:

```py
for x in [0, 1, 2]:
  pass
```

## Ex 2: Using the pass keyword in a function definition:

```py
def myfunction():
  pass
```

## Ex 3: Using the pass keyword in a class definition:

```py
class Person:
  pass
```

## Ex 4: Using the pass keyword in an if statement:

```py
a = 33
b = 200

if b > a:
  pass
```
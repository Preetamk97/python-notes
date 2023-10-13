```py
# Keyword Argument : An argument that is preceded by an identifier.
#                    Helps with redability.
#                    Order of arguments doesn't matter.

# 4 TYPES OF ARGUMENTS IN PYTHON:  # POSITIONAL
                                   # DEFAULT
                                   # KEYWORD
                                   # ARBITRARY


def hello(greeting, title, firstName, lastName):
    print(f"{greeting} {title}{firstName} {lastName}")

hello("Hello", "Mr.", "Pritam", "Kalita")   # Positional Arguments
# Hello Mr.Pritam Kalita

hello("Pritam", "Mr.", "Hello", "Kalita")      # Order of arguments 
#                                                matters with Positional Arguments
# Pritam Mr.Hello Kalita

hello(greeting="Hello", title="Mr.", firstName="Pritam", lastName="Kalita")     # Keyword Arguments
# Hello Mr.Pritam Kalita

hello(firstName="Pritam", title="Mr.", greeting="Hello", lastName="Kalita")      # Order of arguments doesn't  
#                                                                                  matter with Keyword Arguments
# Hello Mr.Pritam Kalita



# Keyword Arguments Found Within print() Statement:
#**************************************************
# 1. 'end' 
for x in range(1,11): 
    print(x, end=" ")
print()
# 1 2 3 4 5 6 7 8 9 10

# 2. 'sep' (separate)
print("1","2","3","4","5","6","7","8", sep="-")
# 1-2-3-4-5-6-7-8
```
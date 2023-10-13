```py
# *args     = allows you to pass multiple non-keyword arguments
# **kwargs  = allows you to pass multiple keyword-arguments
#             '*' is called unpacking operator   
# 4 TYPES OF ARGUMENTS IN PYTHON:  # POSITIONAL
                                   # DEFAULT
                                   # KEYWORD
                                   # ARBITRARY**


# Example 1: Use of '*args'
# *************************
def sum(*args):         # (*args) means that the function can accept any number of non-keyword arguments.
    total = 0            
    for arg in args:        
        total = total+arg
    print(total)

sum(1,2,3,4,5,6,7,8,9,10)   # (1,2,3,4,5,6,7,8,9,10) are non-keyword arguments
# 55


# Example 2: Use of '*args'
# *************************
def print_full_name(*args):
    for arg in args:
        print(arg, end=" ")

print_full_name("Pritam", "Ranjan", "Kalita")
# Pritam Ranjan Kalita


print()


# Example 3: Use of '**kwargs'
# ****************************
def print_address(**kwargs):
    # When we pass multiple "keyword-arguments" - inside a function - using "**kwargs" argument
    # the Python Interpreter, interprets the complete set of  keyword-arguments  passed
    # as a big-single 'Python Dictionary'.
    for key,value in kwargs.items():
        print(f"{key} : {value}")

print_address(houseNo="30", 
              street="Adarshapur Lane-4", 
              locality="Kalyani Nagar, Kahilipara", 
              city="Guwahati", 
              state="Assam", 
              pin="781019")             # These are keyword arguments
# houseNo : 30
# street : Adarshapur Lane-4
# locality : Kalyani Nagar, Kahilipara
# city : Guwahati
# state : Assam
# pin : 781019


# ----- EXERCISE -----
# *********************
def shipping_label(*args, **kwargs):        # Using *args & **kwargs together
    for arg in args:
        print(arg, end=" ")
    print()

    if "apartment" in kwargs:       # If 'apartment' key is present in 'kwargs' dictionnary
        print(f"{kwargs.get('apartment')}")
        print(f"{kwargs.get('street')}")
    elif "pobox" in kwargs:         # ElseIf 'pobox' key is present in 'kwargs' dictionnary
        print(f"{kwargs.get('street')}")
        print(f"{kwargs.get('pobox')}")
    else:
        print(f"{kwargs.get('street')}")

    print(f"{kwargs.get('city')}, {kwargs.get('state')} {kwargs.get('zip')}")


shipping_label("Dr.", "Spongebob", "Squarepants",
               street="123 Fake St.",
               pobox="PO box #1001",
               city="Detroit",
               state="MI",
               zip="54321")
# Dr. Spongebob Squarepants
# 123 Fake St.
# PO box #1001
# Detroit, MI 54321
```
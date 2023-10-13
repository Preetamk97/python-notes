```py
# Order of Proirity of Varible Scopes : LOCAL > ENCLOSED > GLOBAL > BUILT-IN


# ----- Scope : LOCAL VARIABLE-----

def func1():
    x = 1 # local
    print(x)

def func2():
    x = 2 # local
    print(x)

func1()
func2()

# ----- Scope : ENCLOSED VARIABLE -----

def func1():
    x = 1 # enclosed

    def func2():
        # no local variable here
        # when it does not find any Local variable, it will look for any Enclosed variable.
        print(x)
    func2()

func1()

# ----- Scope : GLOBAL VARIABLE -----

x = 3 #global

def func1():
    print(x)

def func2():
    print(x)

func1()
func2()

# ----- Scope : BUILT-IN VARIABLE -----

from math import e  # Built-in

def func1():
    print(e)

func1()


# ----- Order of Proirity : GLOBAL > BUILT-IN  DEMO ----- #
from math import e  # BUILT-IN

e = 5               # GLOBAL

def func1():
    print(e)

func1()
# 5
# Order of Proirity : GLOBAL > BUILT-IN
```
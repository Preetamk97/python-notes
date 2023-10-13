```py
# There are 3 logical operators in Python - 'and', 'or', 'not'

# 'and' operator example
#*******************************************************************************

temp = 20

if (temp>10 and temp<=25):
    print("Temperature is good")
else:
    print("Temperature is bad")

# Temperature is good


# 'or' operator example
#********************************************************************************

temp = 25

if (temp<=0 or temp>=30):
    print("Temperature is bad")
else:
    print("Temperature is good")

# Temperature is good


# 'not' operator example
#********************************************************************************

sunny = True

if not sunny:   # If 'sunny' is not True
    print("It is cloudy outside")
else:
    print("It is sunny outside !")

# It is sunny outside ! 


sunny = False

if not sunny:   # If 'sunny' is not True
    print("It is cloudy outside")
else:
    print("It is sunny outside !")

# It is cloudy outside
```
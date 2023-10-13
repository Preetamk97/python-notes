## `return`  = statement used to end a function and return a result back to the caller
<br>

# Example 1: Happy Birthday 

```py
def happy_birthday(name, age):
    print(f"Happy Birthday to {name}!")
    print(f"You are {age} years old now !")
    print(f"Wish you a lots of Happiness, Sucess and Abundance")

happy_birthday("Pritam", 26)
# Happy Birthday to Pritam!
# You are 26 years old now !
# Wish you a lots of Happiness, Sucess and Abundance
```

# Example 2: Adding 2 Numbers

```py
num1 = int(input("Enter 1st number : "))
num2 = int(input("Enter 2nd number : "))

def sum_of_two_nos(x,y):
    total = x+y
    return total

result = sum_of_two_nos(num1, num2)

print(f"Sum of both the numbers is {result}")
# Enter 1st number : 5
# Enter 2nd number : 11
# Sum of both the numbers is 16
```

# Example 3: Make Full Name 

```py
first_name = input("Enter First Name : ")
last_name = input("Enter Last Name : ")

def full_name(para_first_name, para_last_name):     # parameters
    para_first_name = str(para_first_name.capitalize())
    para_last_name = str(para_last_name.capitalize())
    return para_first_name + " " + para_last_name     # Python will return this all as a Single String


result = full_name(first_name, last_name)   # arguments     # 'first_name' & 'last_name' are POSITIONAL ARGUMENTS

print(f"Your full name is : {result}")


# Sample Output
# **************

# Enter First Name : pritam
# Enter Last Name : kalita
# Your full name is : Pritam Kalita
```
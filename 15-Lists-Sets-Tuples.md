```py
# collection = a single "variable" used used to store multiple values
#   Tuple = () ordered and unchangeable. Duplicates OK. FASTER Than LIST
#   List  = [] ordered and changeable. Duplicates OK
#   Set   = {} unordered and unchangeable, but Add/Remove OK. NO duplicates
#   Dictionary


# Lists :
# **********************************************************************************************
fruits = ["apple", "banana", "orange", "pineapple" ]

print(fruits)
# ['apple', 'banana', 'orange', 'pineapple']
print(fruits[0])    
# apple
print(fruits[1])
# banana
print(fruits[2])
# orange
print(fruits[:3])   # first 3 elements
# ['apple', 'banana', 'orange']
print(fruits[::-1])     # complete list reverse and print
# ['pineapple', 'orange', 'banana', 'apple']
print(fruits[::2])     # every "jump 2" element from the start
# ['apple', 'orange']


# Printing list of methods available for the List 'fruits'.
# print(dir(fruits))

# Printing description of each of the methods available for the list 'fruits'
# print(help(fruits))


# To check if an element is present in the List 'fruits' - 'in' Operator.
print("apple" in fruits)
# True
print("mango" in fruits)
# False 


# Lists are changeable - after their creation  +  Duplicates are allowed.
fruits = ["apple", "banana", "orange", "pineapple" ]
fruits[1] = "pineapple"
print(fruits)
# ['apple', 'pineapple', 'orange', 'pineapple']


# append() : used to add an item to the end of the list
fruits = ["apple", "banana", "orange", "pineapple" ]
fruits.append("mango")
print(fruits)
# ['apple', 'banana', 'orange', 'pineapple', 'mango']


# remove() : used to remove an item from the end of the list
fruits = ["apple", "banana", "orange", "pineapple" ]
fruits.remove("orange")
print(fruits)
# ['apple', 'banana', 'pineapple']


# insert(index, value): lets you insert a 'value' at any given 'index' of the list
fruits = ["apple", "banana", "orange", "pineapple" ]
fruits.insert(2, "strawberry")
print(fruits)
# ['apple', 'banana', 'strawberry', 'orange', 'pineapple']


# sort(): sorts a list in alphabetical order
fruits = ["pineapple", "banana", "orange", "apple"]
fruits.sort()
print(fruits)
# ['apple', 'banana', 'orange', 'pineapple']


# reverse(): reverses the list
fruits = ["pineapple", "banana", "orange", "apple"]
fruits.reverse()
print(fruits)
# ['apple', 'orange', 'banana', 'pineapple']


# clear() : empties a list
fruits = ["pineapple", "banana", "orange", "apple"]
fruits.clear()
print(fruits)
# []


# Getting the index number of an element in list
fruits = ["pineapple", "banana", "orange", "apple"]
print(fruits.index("apple"))
# 3


# Getting the 'number of occurences'/count of an element in list
fruits = ["pineapple", "banana", "orange", "apple"]
print(fruits.count("apple"))
# 1


# Length of a list
print(len(fruits))
# 4



# Sets:
# ***********************************************************************************************

fruits = {"apple", "banana", "orange", "pineapple"}

# Set is unordered - it does not maintain the order of insertion
print(fruits)
# {'banana', 'orange', 'pineapple', 'apple'}

# No duplicates are allowed:
fruits = {"apple", "banana", "orange", "pineapple", "pineapple"}
print(fruits)
# {'banana', 'apple', 'orange', 'pineapple'}

# print(dir(fruits))
# print(help(fruits))
print(len(fruits))      # 4
print("pineapple" in fruits)        # True


# We cannot use indexing on a Set because, Sets are unordered.
# Below line will give error
# print(fruits[0])
# TypeError: 'set' object is not subscriptable


# We can add or remove elements to a Set
fruits = {"apple", "banana", "orange", "pineapple"}
fruits.add("mango")
fruits.remove("orange")
print(fruits)
# {'pineapple', 'apple', 'banana', 'mango'}


# pop() : randomly removes any one element from the Set
fruits = {"apple", "banana", "orange", "pineapple"}
fruits.pop()
print(fruits)
# {'pineapple', 'banana', 'orange'}


# clear(): empties the Set
fruits = {"apple", "banana", "orange", "pineapple"}
fruits.clear()
print(fruits)
# set()



# Tuples:
# ************************************************************************************************

fruits = ("apple", "banana", "orange", "pineapple", "pineapple")

print(fruits)
# ('apple', 'banana', 'orange', 'pineapple')

# print(dir(fruits))
# print(help(fruits))
print(len(fruits))      # 4
print("pineapple" in fruits)        # True


# count():
print(fruits.count("pineapple"))
# 2

# index():
print(fruits.index("apple"))
# 0
```
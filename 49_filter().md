```py
# filter() =    creates a collection of elements from an iterable (List/Tuple/Set),
#               for which a function returns 'true'
#
#               filter(function, iterable)

# Here is a list of some 'friends' characters with their ages - It is a 'List' of 'Tuples'
friends = [("Rachel",19),
           ("Monica",18),
           ("Phoebe",17),
           ("Joey",16),
           ("Chandler",21),
           ("Ross",20)]

# Lets us create a separate new list for those 'friends' list elements whose age is greater than or equal to 18.

# function for filtering the elements (whose age is greater than or equal to 18)
age = lambda data:data[1] >= 18

# filter(filter_function, iterable)  --> returns a filter object which can be then typecasted to any iterable.
drinking_buddies = list(filter(age, friends))   # filter object typecasted to list

for i in drinking_buddies:
    print(i)
# ('Rachel', 19)
# ('Monica', 18)
# ('Chandler', 21)
# ('Ross', 20)
```
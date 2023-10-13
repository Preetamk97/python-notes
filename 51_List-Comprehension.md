```py
# list comprehension =  a programming technique to create a new list with less syntax
#                       list = [expression for item in range]
#                       list = [expression for item in iterable]
#                       list = [expression for item in iterable (if conditional)]
#                       list = [expression (if/else  conditional) for item in iterable]


# Example 1: Creating a list of Squares of numbers from range(1,10)
###################################################################

# Using for loop
#-----------------
squares = []                # create an empty list
for i in range(1,11):       # create a for loop
    squares.append(i * i)    # define what each loop iteration should do
print(squares)
# [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# Using List Comprehension Technique
#------------------------------------
squares = [i * i for i in range(1,11)]      # list = [expression for item in range]
print(squares)
# [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]


# Example 2: Creating a List of marks >= 60 from a given list of marks.
#######################################################################

marks = [100,90,80,70,60,50,40,30,0]    

# Using filter function
#------------------------
filtered_marks = list(filter(lambda x: x >= 60, marks))


# Using List Comprehension
#--------------------------

# list = [expression for item in iterable (if conditional)]
filtered_marks = [i for i in marks if i >= 60]   
print(filtered_marks)
# [100, 90, 80, 70, 60]

# list = [expression (if/else  conditional) for item in iterable]
filtered_marks = [i if i >= 60 else "FAILED" for i in marks]
print(filtered_marks)
# [100, 90, 80, 70, 60, 'FAILED', 'FAILED', 'FAILED', 'FAILED']
```
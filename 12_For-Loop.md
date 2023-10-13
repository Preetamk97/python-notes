# Example:

```py
# Counting Forwards
# *****************
for x in range(1, 11):
    print(x)    # This will print values from 1-10
print ("Happy New Year !")
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
# Happy New Year !


# Counting Backwards
# ******************
for x in reversed(range(1, 11)):
    print(x)    # This will print values from 10-1
print ("Happy New Year !")
# 10
# 9
# 8
# 7
# 6
# 5
# 4
# 3
# 2
# 1
# Happy New Year !


# Counting in Steps
# *****************
for x in range(1, 11, 2):  
    print(x)    # This will print values from 1-10 -> in steps of 2.
print ("Happy New Year !")
# 1
# 3
# 5
# 7
# 9
# Happy New Year !


# Printing in Same Line in Python: Use of 'end' attribute
# *******************************************************

print("This is an example")
print("Of printing in different lines in Python")
# This is an example
# Of printing in different lines in Python

print("This is an example", end=" ")
print("Of printing in same line in Python")
# This is an example Of printing in same line in Python

print("This is an example", end="\n\n")
print("Of printing in same line in Python")
# This is an example

# Of printing in same line in Python

print("This is an example", end="++++++")
print("Of printing in same line in Python")
# This is an example++++++Of printing in same line in Python


# Iterating over a String
# ***********************
name = "Pritam-Ranjan-Kalita"

for x in name:
    print(x, end=" ")   # Printing the values in same line - each followed by a space.

# P r i t a m - R a n j a n - K a l i t a
```
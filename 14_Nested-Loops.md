```py
# nested loop = loop within another loop 
#                          outer loop:
#                              inner loop:

# Example 1:
# **********

# for x in range(1,4):      # 1 - 2 - 3     # 3 times
for x in range(3):          # 0 - 1 - 2     # 3 times
    for y in range(1,10):
        print(y, end="")

    print()  
    # starts a new line after complete execution of each 'for y' loop 
    # is within the 'for x' loop.

# Output:
# -------
# 123456789
# 123456789
# 123456789


# Example 2:
# **********

# for x in range(1,4):      # 1 - 2 - 3     # 3 times
for x in range(3):          # 0 - 1 - 2     # 3 times
    # for y in range(1,10):
    for y in range(10):     # 0 - 9         # 10 times
        print(y, end="")

    print()

# Output:
# -------
# 0123456789
# 0123456789
# 0123456789


# Example 3: 
# **********

rows = int(input("Enter the # of rows: "))      # 4
columns = int(input("Enter the # of columns: "))    # 10
symbol = input("Enter a symbol to use: ")   # $

for x in range(rows):
   for y in range(columns):
       print(symbol, end="")
   print()

# $$$$$$$$$$
# $$$$$$$$$$
# $$$$$$$$$$
# $$$$$$$$$$
```

# Output:

![](img\chap14\2023-04-24-11-52-05.png)
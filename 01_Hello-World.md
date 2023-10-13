# Why you need to learn Python ?

![](img\chap1\2023-04-07-10-17-05.png)


# Environmment Setup

- Download **Python Interpreter** from **python.org** and install it.
- In your **VS Code** Ide, install the **Python** and **Pylance** Extensions.


# Printing "Hello World !" to console:

```py
print("Hello World !")
print("Nice to meet you !")

# Also this is how you do Single-line Comment in Python. Very important for taking notes !
# And oh ! There is no concept of 'Multi-line Commenting' in python. 
```

![](img\chap1\2023-04-10-22-12-33.png)



# Printing in Same Line in Python: Use of `end` attribute

Observe the below code and the corresponding outputs to know about the use of **'`end`'** attribute inside `print()` method.

```py
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
```
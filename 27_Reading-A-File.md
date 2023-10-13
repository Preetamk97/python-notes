```py
# Reading a file in Python
with open("G:\MY NOTES\PYTHON_NOTES\play\hello.txt") as file:
    print(file.read())

# Hello World !
# Nice to meet you !
# You are very beautiful !

# In Python, files are automatically closed after they are completely read by the Program.
```

```py
try:
    with open("G:\MY NOTES\PYTHON_NOTES\play\hello.txt") as file:
        print(file.read())
except FileNotFoundError:       # This error will occur if the given file address is not found
    print("This file does not exist.. Sorry !")
```
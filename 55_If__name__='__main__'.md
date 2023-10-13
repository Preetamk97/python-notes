Syntactically, Python’s `if __name__ == "__main__"` idiom is just a normal conditional block:

```py
if __name__ == "__main__":
    ...
```

# In Short: It Allows You to Execute Code When the File Runs as a Script, but Not When It’s Imported as a Module

You can think of the conditional block that you open with `if __name__ == "__main__"` as a way to store code that should only run when your file is executed as a script.


# Example 1:

## `module1.py`:

```py
def main():
    print("Hello!")

# Python assigns the value of variable  __name__ = "__main__" for the current-directly-running python script only.
# print(__name__)
# __main__

# Below lines of code will execute only if the module1.py code is ran as a current-directly-running python script.
if __name__ == '__main__':
    print("Running module1.py script directly")
    main()
else:
    print("Running module1.py script indirectly")

# Running module1.py script directly
# Hello!
```

## module2.py

```py
# importing module1.py as module
import module1

# Output 1:
# Running module1.py script indirectly

# Python assigns the value of variable  __name__ = "__main__" for the current-directly-running python script only.
print(__name__)         # Checking the value of __name__ for the current-directly-running python script
# Output 2:
# __main__      

print(module1.__name__)    # Checking the value of __name__ for the imported module 'module1' 
# Output 3:
# module1 


if __name__ == '__main__':
    print("Running module2.py script directly")
else:
    print("Running module2.py script indirectly") 

# Output 4:
# Running module2.py script directly
```
```py
# to work with files - we need to import the 'os' module
import os

# In this program, we will be checking if a file/folder is present at a given location in our system or not.

# Path/location of the file/folder
# We wanna check if this file (hello.txt) exists in this given location (G:\MY NOTES\PYTHON_NOTES\play) or not.
# path = "G:\MY NOTES\PYTHON_NOTES\play\hello.txt"
path = "G:\MY NOTES\PYTHON_NOTES\play\hello"

if os.path.exists(path):                    # If the path given exists
    print("This path exists")
    if os.path.isfile(path):                    # If 'hello.txt' is a file
        print("This is a file")
    elif os.path.isdir(path):                   # If 'hello.txt' is a folder/directory
        print("This is a folder/directory")
else:                                       # If the path given does not exist
    print("This path does not exist")
```
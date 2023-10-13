```py
import os       # This module provides functions for deleting files and empty folders/directories.
import shutil   # This module provides function for deleting non-empty folders/directories
#
#
# Create a file 'test.txt' in the same folder containing play.py file.
# Create an empty folder 'test_empty_folder' in the same folder containing play.py file.
# Create a non-empty folder 'test_not_empty_folder' in the same folder containing play.py file -> Inside that just create a .txt file - to make the 'test_not_empty_folder' really non-empty - you can name it anything.
#
# 
# Address of the file you want to delete
# file_address = "G:\\MY NOTES\\PYTHON_NOTES\\play\\test.txt"                 # file
# file_address = "G:\\MY NOTES\\PYTHON_NOTES\\play\\test_empty_folder"        # empty folder
file_address = "G:\\MY NOTES\\PYTHON_NOTES\\play\\test_not_empty_folder"    # non-empty folder

try:
    # os.remove(path) : can delete only a file 
    os.remove(file_address) 

except FileNotFoundError:                                   # If the file is not found then we get this error
    print(f"{file_address} : File does not exist.")

except PermissionError:                                     # This error occurs because os.remove() cannot
                                                            # delete an empty folder
    # os.rmdir() : deletes an empty folder/directory
    os.rmdir(file_address)                                  
    print("OOPS! This was an empty folder. But dont worry I took care of it :D")
    print(f"Your file \"{file_address}\" has been deleted successfully.") 

except OSError:                                             # This error occurs because os.remove() cannot 
                                                            # delete a non-empty folder
    # shutil.rmtree() : deletes a non-empty folder/directory
    shutil.rmtree(file_address)
    print("OOPS! This was a non-empty folder. But dont worry I took care of it :D")
    print(f"Your file \"{file_address}\" has been deleted successfully.") 
    
else:                                                       # This block executes only if there is no exception 
    print(f"Your file \"{file_address}\" has been deleted successfully.")    
```
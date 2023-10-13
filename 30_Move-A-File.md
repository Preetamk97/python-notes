```py
import os
#
#
# Create a file 'test.txt' in the same folder containing play.py file.
#
# 
source_address = "G:\\MY NOTES\\PYTHON_NOTES\\play\\test"             # Address of the file you want to move
destination_address = "G:\\MY NOTES\\PYTHON_NOTES\\test"        # Address of where you want the file to move


try:
    # If there is already a file with the same name in the destination folder
    if os.path.exists(destination_address):
        print("File with the same name already exists at the destination folder")
    else:
        os.replace(source_address, destination_address)
        print(f"{source_address}  file was removed")
except FileNotFoundError:
    print(f"{source_address} : File does not exist.")

#
#
# NOTE: Here, we have moved a file. But you can also move a folder/directory in the same manner.
#
#
```
```py
# copyfile() =  copies contents of a file
# copy() =       copyfile() + permission mode + destination can be a directory
# copy2() =     copy() + copies metadata (file’s creation and modification times)

import shutil   # shutil module provides function for copying a file

# shutil.copyfile("copy-from-file-address", "copy-to-file-address")
shutil.copyfile("G:\\MY NOTES\\PYTHON_NOTES\\play\\test.txt","G:\\MY NOTES\\PYTHON_NOTES\\play\hello\\copyfile.txt")
# shutil.copy("copy-from-file-address", "copy-to-file-address")
shutil.copy("G:\\MY NOTES\\PYTHON_NOTES\\play\\test.txt","G:\\MY NOTES\\PYTHON_NOTES\\play\hello\\copy.txt")
# shutil.copy2("copy-from-file-address", "copy-to-file-address")
shutil.copy2("G:\\MY NOTES\\PYTHON_NOTES\\play\\test.txt","G:\\MY NOTES\\PYTHON_NOTES\\play\hello\\copy2.txt")
```
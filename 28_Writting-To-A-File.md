# Code 1: Creating A New File And Writing To It / Overwriting Already Existing File

```py
text = "My name is Pritam Ranjan Kalita\nNice to meet you !\nKonichiwa !"
# If we change the text, it will just overwrite the complete original file.

with open("G:\\MY NOTES\\PYTHON_NOTES\\play\\test.txt", 'w') as file:     # In - open("test.txt", 'w') - 'w'        
                                                                          # signifies "write mode"
                                        # By default, open("test.txt") = open("test.txt", 'r')  -  where
                                        # 'r' signifies "read mode"
    file.write(text)


# This creates a file test.txt inside the (G:\MY NOTES\PYTHON_NOTES\play) folder.
```

# Output 1:

![](img\chap28\2023-05-02-21-47-18.png)


# Code 2: Appending To An Already Existing File

```py
text = "\n\nNice meeting you! Bye Bye !"

with open("G:\\MY NOTES\\PYTHON_NOTES\\play\\test.txt", 'a') as file:       # 'a' stands for 'Append' Mode.
    file.write(text)


# This appends the 'text' String to the already existing test.txt file without completely overwriting it again.
```

# Output 2:

![](img\chap28\2023-05-02-21-56-56.png)
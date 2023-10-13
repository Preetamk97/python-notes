# Basic String Methods:

```py
# String Methods
#************************************************************************************************************

name = "Pritam Kalita"

# len(str): returns the length (int) of a string 
print(len(name)) 
#13


# name.find(char or string): returns the index position (int) of the first occurence of the character given as argument.
print(name.find('tam'))
# 3
print(name.find("K"))
# 7
print(name.find("o"))
# -1
# If the program cannot find the character or string, that you pass as argument, then it will return -1.


# name.rfind(char or string): returns the index position (int) of the last occurence of the character given as argument
print(name.rfind('a'))  # printing the last occurence index position of the character 'a' 
#12


# name.capitalize() : Capitalizes only the first letter of the string
print(name.capitalize())
# Pritam kalita


# name.upper() : converts the whole string to uppercase
print(name.upper())
# PRITAM KALITA


# name.lower() : converts the whole string to lowercase
print(name.lower())
# pritam kalita


# name.isdigit() : returns 'True' if the string contains only digits and nothing else
age = "26"
print(age.isdigit())    # True
print(name.isdigit())   # False


# name.isalpha() : returns 'True' if the string contains only alphabets and nothing else
print(name.isalpha())
# False
# Because the {name = "Pritam Kalita"} contains a whitespace(" ") which is not an alphabet


# name.count(char) : returns the total number of occurences in the complete string 
print(name.count("a"))  # counting the number of times 'a' has occured in the string {name = "Pritam Kalita"}
# 3


# name.replace(str1, str2): replaces str1 with str2 in the string 'name'
print(name.replace(" ", "___|___"))
# Pritam___|___Kalita


# To get the list of all the string methods available in Python
help(str)
```

# Username Validation Excercise

```py
# -------------------------------
#        EXERCISE
# -------------------------------
username = input("Enter a username: ")


if len(username) > 12:  # if the length of the string entered is more than 12 characters
   print("Your name can't be more than 12 characters")
elif not username.find(" ") == -1:  # if the username contains any spaces
   print("Your username can't contain spaces")
elif not username.isalpha():    # if the username contains any digits (or spaces)
   print("Your username can't contain digits")
else:
   print(f"Welcome {username}!")
```
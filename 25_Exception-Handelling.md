```py
# exception =   events detected during execution that interrupt the flow of a program

try:
    numerator = int(input("Enter a number to divide: "))
    denominator = int(input("Enter a number to divide by: "))
    result = numerator / denominator
except ZeroDivisionError as e:                      # This exception occurs when we try to divide a number by zero.                      
                                                    # This is the catch block for 'ZeroDivisionError' Exception
                                                    # 'e' is just a nickname for "ZeroDivisionError"
                                                    # 'as e' is just added as a convention and can be
                                                    #  totally ommitted

    print(e)    # This prints the error message - "division by zero"                         
    print("You can't divide by zero! idiot!")
except ValueError as e:                             # ValueError Exception occurs when we provide a String 
                                                    # instead of an integer to divide

    print(e)    # Prints the error message - "invalid literal for int() with base 10: <your input>"
    print("Enter only numbers plz")
except Exception as e:
    print(e)
    print("something went wrong :(")
else:                                               # If no exception occurs then only
    print(result)
finally:                                            # This block will execute always
    print("This will always execute")               
```
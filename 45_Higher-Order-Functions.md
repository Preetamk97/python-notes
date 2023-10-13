```py
#  Higher Order Function =  A function that either:
#                           1. accepts a function as an argument
#                               or
#                           2. returns a function
#                           (In python, functions are also treated as objects)

# ----- 1. accepts a function as an argument ----- 
def loud(text):
   return text.upper()

def quiet(text):
   return text.lower()

def hello(func):
   text = func("Hello")     # Giving string "Hello" as argument to whatever function this hello(func) function #                          gets as an argument. Whatever value is returned gets stored inside 'text' variable.
   print(text)


hello(loud)                 # Giving function loud() as argument
hello(quiet)                # Giving function quiet() as argument


# ------------ 2. returns a function ------------- 
def numerator(x):
   
   def denominator(y):      # denominator() function inside numerator() function
       division = y / x
       return division
   
   return denominator       # The numerator() function is returning denominator() function


answer = numerator(2)       # Here, the numerator(x = 2) function is returning denominator(y) function inside
                            # the 'answer' variable + the value for x = 2 is stored in temporary memory until the execution of the entire numerator(x) function is complete to the end.
print(answer(10))           # answer(10) = numrator(2){denominator(10)}
```
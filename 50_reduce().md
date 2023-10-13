```py
# reduce() = Applies a function to an iterable and reduces it to a single cumulative value.
#            Performs function on the first two elements and keeps repeating the same process until 1 value 
#            remains.
#
# reduce(function, iterable)

import functools            # Necessary import for using reduce()

letters = ["H","E","L","L","O"]

word = functools.reduce(lambda x, y : x + y,letters)
# What is happening here is that reduce() function is applying the - lambda x, y : x + y - function on the 'letters' list repeatedly - taking two list elements at a time - starting from the first 2 elements of the list - until all the elements get reduced to a single output - then this single output (lets name it 'final result') is returned by the functools.reduce() method - and is stored inside the 'word' variable.
# 1st Iteration --> "H","E" : "H" + "E" --> "HE"
# 2nd Iteration ---> "HE","L": "HE" + "L" ---> "HEL"
# 3rd Iteration ---> "HEL","L" : "HEL" + "L"  ---> "HELL"
# 4th Iteration ---> "HELL","O" : "HELL" + "O"  ---> "HELLO"
# final result = "HELLO" = returned by functools.reduce()
print(word)

# Another Example
factorial = [5,4,3,2,1]    
result = functools.reduce(lambda x, y : x * y,factorial)    # This will return the result of 5! inside result
# 1st Iteration --> 5,4 : 5*4 --> 20
# 2nd Iteration ---> 20,3: 20*3 ---> 60
# 3rd Iteration ---> 60,2 : 60*2  ---> 120
# 4th Iteration ---> 120,1 : 120*1  ---> 120
# final result = 120 = returned by functools.reduce()
print(result)
```
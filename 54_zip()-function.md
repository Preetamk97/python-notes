```py
# zip(*iterables) =  returns a zip object which contains tuples - with each tuple contaning 1 element from each 
#                    of the iterables given as argument to the zip() function - in sequential order.

# iterables passed to zip() function as arguments can be lists, tuples, sets or mix of them.
# The returned zip object can be directly stored inside any variable 
# The returned zip object can be converted to any iterable type (list/set/tuple/dict).


usernames = ["Dude", "Bro", "Mister"]               # List
passwords = ("p@ssword", "abc123", "guest")         # Tuple
login_dates = ["1/1/2021","1/2/2021","1/3/2021"]    # List

# ---------------------------------------------------------------------------------------------


# Example 1
# ---------------------------------------------------------------------------------------------
users = list(zip(usernames,passwords)) 
# iterables passed to zip() function as arguments can be lists, tuples, sets or mix of them. 
# The returned zip object can be converted to any iterable type (list/set/tuple).
# 'zip' object is converted to 'list' iterable and stored inside 'users'
# 'users' is a 'list' of 'tuples'

for i in users:
    print(i)
# ('Dude', 'p@ssword')
# ('Bro', 'abc123')
# ('Mister', 'guest')


# Example 2
# --------------------------------------
users = dict(zip(usernames,passwords))
# iterables passed to zip() function as arguments can be lists, tuples, sets or mix of them.    
# If there are only iterables as arguments, the zip object can also be converted to a dictionary.
# 'users' is a dictronary now

for key,value in users.items():
    print(key+" : "+value)
# Dude : p@ssword
# Bro : abc123
# Mister : guest


# Example 3
# --------------------------------------
users = zip(usernames,passwords,login_dates)
# Iterables passed to zip() function as arguments can be lists, tuples, sets or mix of them. 
# Any number of iterbales can be passed inside zip() function
# The returned zip object can be directly stored inside any variable 
# 'users' is a zip() object containing tuples

for i in users:
    print(i)
# ('Dude', 'p@ssword', '1/1/2021')
# ('Bro', 'abc123', '1/2/2021')   
# ('Mister', 'guest', '1/3/2021') 

# --------------------------------------
```
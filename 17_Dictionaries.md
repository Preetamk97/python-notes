```py
# Dictionary = colection of {key:value} pairs
#            = ordered and changeable. NO DUPLICATE KEYS.

capitals = {"USA":"Washington DC",
            "India":"New Delhi",
            "Canada":"Ottawa",
            "Russia":"Moscow",
            "Russia":"Stanlingrad"}

print(capitals)
# {'USA': 'Washington DC', 'India': 'New Delhi', 'Canada': 'Ottawa', 'Russia': 'Stanlingrad'}

# print(dir(capitals))    # Printing the list of all available methods for the 'capitals' dictionary.
# help(capitals)            # Printing the details of all available methods for the 'capitals' dictionary.

# get(key): returns the value associated with the key 
print(capitals.get("USA"))
# Washington DC

# If we try to get the value for a key that does not exist in the dictionary the dictionary then the output will be 'None'
print(capitals.get("Japan"))
# None


# Checking if a key is our dictionary
if capitals.get("Japan"):
    print("That capital exists in our dictionary")
else:
    print("That capital does not exist in our dictionary")
# That capital does not exist in our dictionary


# Adding {key:value} pairs to our dictionary
capitals.update({"Japan":"Tokyo"})
print(capitals)
# {'USA': 'Washington DC', 'India': 'New Delhi', 'Canada': 'Ottawa', 'Russia': 'Stanlingrad', 'Japan': 'Tokyo'}

# Updating {key:value} pairs to our dictionary
capitals.update({"India":"Mumbai"})
print(capitals)
# {'USA': 'Washington DC', 'India': 'Mumbai', 'Canada': 'Ottawa', 'Russia': 'Stanlingrad', 'Japan': 'Tokyo'}

# Removing a {key:value} pair
capitals.pop("Russia")
print(capitals)
# {'USA': 'Washington DC', 'India': 'Mumbai', 'Canada': 'Ottawa', 'Japan': 'Tokyo'}


# popitem(): removes the last {key:value} pair.
capitals.popitem()
print(capitals)
# {'USA': 'Washington DC', 'India': 'Mumbai', 'Canada': 'Ottawa'}

# clear(): clears the complete dictionary
capitals.clear()
print(capitals)
# {}


# keys(): gives set of all the 'keys' from the dictionary
capitals = {"USA":"Washington DC",
            "India":"New Delhi",
            "Canada":"Ottawa",
            "Russia":"Moscow",
            "Russia":"Stanlingrad"}
print(capitals.keys()) 
# dict_keys(['USA', 'India', 'Canada', 'Russia'])

# values(): gives set of all the 'values' from the dictionary
print(capitals.values())
# dict_values(['Washington DC', 'New Delhi', 'Ottawa', 'Stanlingrad'])

# We can also iterate through 'capitals.keys()' & 'capitals.values()' using a 'for' loop
for key in capitals.keys():
    print(key)
# USA
# India
# Canada
# Russia


# .items():
print(capitals.items())
# dict_items([('USA', 'Washington DC'), ('India', 'New Delhi'), ('Canada', 'Ottawa'), ('Russia', 'Stanlingrad')])

for (key, value) in capitals.items():
    print(f"{key}:{value}")
# USA:Washington DC
# India:New Delhi
# Canada:Ottawa
# Russia:Stanlingrad
```
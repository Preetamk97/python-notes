```py
# 2D List = list of lists
# 2D List = [list1, list2, list3, list 4]

            # Col0    Col1    Col2        Col3
fruits = ["apple", "mango", "banana", "pineapple"]      # Row0
vegetables = ["carrot", "potato"]                       # Row1
meat = ["chicken", "fish", "mutton"]                    # Row2

# 2D List
# groceries = [fruits, vegetables, meat]
groceries = [
    ["apple", "mango", "banana", "pineapple"],
    ["carrot", "potato"],
    ["chicken", "fish", "mutton"]
]

print(groceries)
# [['apple', 'mango', 'banana', 'pineapple'], ['carrot', 'potato'], ['chicken', 'fish', 'mutton']]
print(groceries[0])
# ['apple', 'mango', 'banana', 'pineapple']
print(groceries[1])
# ['carrot', 'potato']
print(groceries[2])
# ['chicken', 'fish', 'mutton']


# Printing [Row0][Col2] = "banana"
print(groceries[0][2])
# banana

# Printing [Row2][Col0] = "chicken"
print(groceries[2][0])
# "chicken"


# Using Nested Loops with 2D Lists
for collection in groceries:
    for item in collection:
        print(item, end=" ")
    print()

# apple mango banana pineapple
# carrot potato
# chicken fish mutton


# You can get really creative with 2d Collections in Python
# You can make a 2D Tuple of Lists:
groceries = (
    ["apple", "mango", "banana", "pineapple"],
    ["carrot", "potato"],
    ["chicken", "fish", "mutton"]
)

# Or you can make a 2D Tuple of Tuples:
groceries = (
    ("apple", "mango", "banana", "pineapple"),
    ("carrot", "potato"),
    ("chicken", "fish", "mutton")
)

# Or you can make a 2D Set of Tuples... as per your requirement
groceries = {
    ("apple", "mango", "banana", "pineapple"),
    ("carrot", "potato"),
    ("chicken", "fish", "mutton")
}
```
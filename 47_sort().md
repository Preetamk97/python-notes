```py
# sort() = used ONLY with lists[]
# sorted() = used with other iterables (Tuples/Sets)

# Sorting a simple list[] : Using sort()
students = ["Squidward", "Patrick", "Sandy", "Spongebob", "Mr.Krabs"]

students.sort()     # Sorts the list in ascending order
print(students)     # ['Mr.Krabs', 'Patrick', 'Sandy', 'Spongebob', 'Squidward']

# Sorting the list in reverse order : Using sort(reverse=True)
students.sort(reverse=True)     
print(students)                 # ['Squidward', 'Spongebob', 'Sandy', 'Patrick', 'Mr.Krabs']


# Sorting a tuple() : Using sorted(iterable)
students = ("Squidward", "Patrick", "Sandy", "Spongebob", "Mr.Krabs")

sorted_students = sorted(students)      # sorted() function accepts an iterable (List/Set) as argument but returns a list
print(sorted_students)                  # ['Mr.Krabs', 'Patrick', 'Sandy', 'Spongebob', 'Squidward']


# print(students.sort())   # This line gives an error as sort() function can only be used with Lists 
#                            (and not Tuples or Sets)


# Sorting the tuple in reverse order : Using sorted(iterable, reverse=True)
reverse_sorted_students = sorted(students, reverse=True)
print(reverse_sorted_students)          # ['Squidward', 'Spongebob', 'Sandy', 'Patrick', 'Mr.Krabs']


# Sorting a set : Using sorted(iterable)
students = {"Squidward", "Patrick", "Sandy", "Spongebob", "Mr.Krabs"}

sorted_students = sorted(students)
print(sorted_students)                  # ['Mr.Krabs', 'Patrick', 'Sandy', 'Spongebob', 'Squidward']


# Sorting the set in reverse order :  Using sorted(iterable, reverse=True)
sorted_students = sorted(students, reverse = True)
print(sorted_students)                  # ['Squidward', 'Spongebob', 'Sandy', 'Patrick', 'Mr.Krabs']



# Sorting a List of Tuples
# ("Name", "Grade", age)
students = [("Squidward", "A", 60),     
            ("Sandy", "A", 33),
            ("Patrick", "D", 36),
            ("Spongebob", "B", 20),
            ("Mr.Krabs", "C", 78)]

# Here we can visualize this 2D list as a collection of 3 columns
# Column 1 : Student names
# column 2 : Student grades
# Column 3 : Student ages

# sorting the list as per column 1 (Student names)
students.sort()
for item in students:
    print(item)
# ('Mr.Krabs', 'C', 78)
# ('Patrick', 'D', 36)
# ('Sandy', 'A', 33)
# ('Spongebob', 'B', 20)
# ('Squidward', 'A', 60)


# sorting the list as per column 2 (Student grades)
students = [("Squidward", "A", 60),     
            ("Sandy", "A", 33),
            ("Patrick", "D", 36),
            ("Spongebob", "B", 20),
            ("Mr.Krabs", "C", 78)]

grade = lambda item:item[1]     # function that returns 'grade' element from from each 'item' tuple of the list
students.sort(key=grade)      
for item in students:
    print (item)
# ('Squidward', 'A', 60)
# ('Sandy', 'A', 33)
# ('Spongebob', 'B', 20)
# ('Mr.Krabs', 'C', 78)
# ('Patrick', 'D', 36)


# sorting the list as per column 3 (Student ages)
students = [("Squidward", "A", 60),     
            ("Sandy", "A", 33),
            ("Patrick", "D", 36),
            ("Spongebob", "B", 20),
            ("Mr.Krabs", "C", 78)]

age = lambda item: item[2]       # function that returns 'age' element from from each 'item' tuple of the list
students.sort(key=age)      
for item in students:
    print (item)
# ('Spongebob', 'B', 20)
# ('Sandy', 'A', 33)
# ('Patrick', 'D', 36)
# ('Squidward', 'A', 60)
# ('Mr.Krabs', 'C', 78)

# We can also reverse this list
students.sort(key=age, reverse=True)
for item in students:  
    print(item)
# ('Mr.Krabs', 'C', 78)
# ('Squidward', 'A', 60)
# ('Patrick', 'D', 36)
# ('Sandy', 'A', 33)
# ('Spongebob', 'B', 20)


# sorting a tuple of tuples 
students = (("Squidward", "A", 60),     
            ("Sandy", "A", 33),
            ("Patrick", "D", 36),
            ("Spongebob", "B", 20),
            ("Mr.Krabs", "C", 78))

grade = lambda item: item[1]
sorted_students = sorted(students, key=grade, reverse=True)     # Sorting as per grades in reverse order
for item in sorted_students:
    print(item)
# ('Patrick', 'D', 36)
# ('Mr.Krabs', 'C', 78)
# ('Spongebob', 'B', 20)
# ('Squidward', 'A', 60)
# ('Sandy', 'A', 33)
```
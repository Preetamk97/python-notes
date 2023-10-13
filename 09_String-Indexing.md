```py
# indexing = accessing elements of a sequence using [] (indexing operator)
# [start_Index : end_Index : step]
# Index number of any sequence in Python always starts from 0.


credit_card_number = "1234-5678-9012-3456"


# Printing the 1st digit of the credit card number 
print(credit_card_number[0])
# 1

# Printing the 1st-4th digits of the credit card number
# The digit with index position 4 is excluded.
print(credit_card_number[0:4])
# 1234

# Printing the 1st-4th digits of the credit card number
# The digit with index position 4 is excluded.
print(credit_card_number[:4])
# 1234

# Printing the 5th-8th digits/characters of the credit card number
# The digit with index position 8 is excluded.
print(credit_card_number[4:8])
# -567

# Printing 'all characters of the sequence' starting from index position 4 (5th character of the sequence) till the end.
print(credit_card_number[4:])
# -5678-9012-3456

# Printing the last character/digit or 1st character from the end.
print(credit_card_number[-1])
# 6

# Printing the last 4 characters/digits.
print(credit_card_number[-4:])
# 3456

# Printing all the digits/characters [from the start : till the end : in steps of 2] 
print(credit_card_number[::2])
# 13-6891-46

# Printing all the digits/characters [from the start : till the end : in steps of 3] 
print(credit_card_number[::3])
# 146-136


# Reversing the entire sequence of 'credit_card_number' string
print(credit_card_number[::-1])
# 6543-2109-8765-4321
```
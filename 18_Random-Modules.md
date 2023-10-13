# Basics:

```py
# importing 'random' module
import random

# To get information on 'random' module
# print(help(random))

# random.randint(): To get a random integer between a given range 
# Example 1: range(1,6)
ran_int = random.randint(1,6)
print(ran_int)
# Example 2: range(low,high)
low = 1
high = 100
ran_int = random.randint(low,high)
print(ran_int)


# random.random(): returns a floating point number between 0 and 1
number = random.random()
print(number)


# random.choice(list/tuple): picks a random element from the given collection everytime
# Example 1:
options = ("rock", "paper", "scissor")
rand_option = random.choice(options)    # Give me a random choice from the 'options' tuple
print(rand_option)

# random.shuffle(list/tuple) : SHuffles the order of the given collection everytime
cards = ["A", "2", "3", "4", "5", "6", "7", "8", "9", "10", "J", "K", "Q"]
random.shuffle(cards) 
print(cards)
```

# Excercise: 'Guess The Number' Game

```py
import random

highest_number = 100
lowest_number = 1
rand_number = random.randint(lowest_number,highest_number)
no_of_guesses = 0

while True:     # This while condition is always True
    guess = int(input(f"Enter your number guess between ({lowest_number}-{highest_number}): "))
    no_of_guesses += 1
    if (guess>rand_number):
        print("Your guess is too high")
    elif(guess<rand_number):
        print("Your guess is too low")
    else: # (guess=rand_number)
        break   # break out of the loop

print("Congratulations ! You got the number correct !")
print(f"No of guesses you took was : {no_of_guesses}")
```
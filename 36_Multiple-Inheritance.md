```py
# Multiple Inheritance: The event when a child class is derived from more than one parent class.

class Prey:

    def flee(self):
        print("This animal flees")

class Predator:

    def hunt(self):
        print("This animal is hunting")

class Rabbit(Prey):                 # Single Inheritance
    pass

class Hawk(Predator):               # Single Inheritance
    pass

class Fish(Prey, Predator):         # Multiple Inheritance
    pass


rabbit = Rabbit()
hawk = Hawk()
fish = Fish()

rabbit.flee()                       # This animal flees
hawk.hunt()                         # This animal is hunting
fish.flee()                         # This animal flees
fish.hunt()                         # This animal is hunting
```
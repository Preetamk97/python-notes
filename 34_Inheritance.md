# `main.py`:

```py
# Parent class
class Animal:
     
    alive = True

    def eat(self):
        print("The animal is eating")

    def sleep(self):
        print("The animal is sleeping")


# Child class 
class Rabbit(Animal):
    # This child class has inherited all the attributes and methods of parent class Animal.
    # Child class can have it own methods.
    def run(self):
        print("The rabbit is running")

# Child class 
class Fish(Animal):
    # This child class has inherited all the attributes and methods of parent class Animal.
    # Child class can have it own methods.
    def swim(self):
        print("The fish is swimming")

# Child class 
class Hawk(Animal):
    # This child class has inherited all the attributes and methods of parent class Animal.
    
    # overiding parent 'Animal' class method eat() - only for Hawk class specifically
    def eat(self):
        print("The hawk is eating")

    # overiding parent 'Animal' class method sleep() - only for Hawk class specifically
    def sleep(self):
        print("The hawk is sleeping")

    # Child class can have it own methods.
    def fly(self):
        print("The hawk is flying")


# Creating objects of Rabbit, Fish & Hawk class
rabbit = Rabbit()
fish = Fish()
hawk = Hawk()

print(rabbit.alive)     # True

rabbit.eat()            # The animal is eating
rabbit.sleep()          # The animal is sleeping
rabbit.run()            # The rabbit is running 

fish.eat()              # The animal is eating
fish.sleep()            # The animal is sleeping'
fish.swim()             # The fish is swimming  

hawk.eat()              # The hawk is eating
hawk.sleep()            # The hawk is sleeping
hawk.fly()              # The hawk is flying
```
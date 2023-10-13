```py
# Multilevel Inheritance : The event when a child class inherits from another child/derived class.

class Organism:

    alive = True


class Animal(Organism):

    def eat(self):
        print("This animal is eating")


class Dog(Animal):

    def bark(self):
        print("This dog is barking")


dog = Dog()         # Creating an object 'dog' of 'Dog' class

print(dog.alive)    # inherited from the Organism class     # True
dog.eat()           # inherited from the Animal class       # This animal is eating
dog.bark()          # defined in Dog class                  # This dog is barking
```
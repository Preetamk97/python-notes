```py
# abstract method = a method that has a declaration but does not have an implementation.
# abstract class = A class which contains ATLEAST 1 OR MORE abstract methods.
#                  Prevents a user from creating an object of that class.
#                  Compels a user to override abstract methods in a child class.

# Concrete classes contains only concrete (normal) methods whereas abstract classes 
# may contain both concrete methods and abstract methods. 


# Necessary Imports for making Abstract Classes
from abc import ABC, abstractmethod

# Abstract class
#################
# The abstract class MUST inherit the in-built ABC class (Abstract Base Class).
class Vehicle(ABC):
    # An Abstract Class must contain ATLEAST one abstract method.

    # Note:
    #######
    # To create an Abstract Method, simply use the @abstractmethod annotation
    # and just keep 'pass' as the method implementation

    # abstract method 1
    @abstractmethod
    def start(self):
        pass
    
    # abstract method 2
    @abstractmethod
    def stop(self):
        pass


# Child Class 1
###############
class Car(Vehicle):
    
    def start(self):                        # implementation of abstract method start()
        print("The car has started")

    def stop(self):                         # implementation of abstract method stop()
        print("The car has stopped")

# Child Class 2
###############
class Motorcycle(Vehicle):

    def start(self):                        # implementation of abstract method start()
        print("The motorcycle has started")

    def stop(self):
        print("The motorcycle has stopped") # implementation of abstract method stop()


# vehicle = Vehicle()     # TypeError: Can't instantiate abstract class Vehicle 
                          # with abstract method start
car = Car()
motorcycle = Motorcycle()

car.start()             # The car has started
car.stop()              # The car has stopped

motorcycle.start()      # The motorcycle has started
motorcycle.stop()       # The motorcycle has stopped
```
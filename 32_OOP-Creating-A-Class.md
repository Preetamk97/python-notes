## It is advisable to create a new module separately for a class. So, create a file `car.py` where we will create a `class Car`.

## `car.py`:

```py
class Car:
    # Attributes
    #############
    # make =  None
    # model = None
    # year =  None
    # color = None

    # We can, but we do not need to declare the attributes in advance 
    # we can declare the attributes of the class directly as pareameters of __init__(self) constructor method

    # Class Constructor
    ####################
    # def __init__(self) :: is a special method which is used as Class Constructor Method in Python
    # 'self' keyword, represents the object of this class 'Car' - that we are currently creating. It is similar to 'this' keyword in java and cpp. 
    # Also, we can declare the attributes of the class for the first time - directly as pareameters of __init__(self) method.
    def __init__(self, make, model, year, color):
        self.make = make
        self.model = model
        self.year = year
        self.color = color

    # Class Method 1 
    #################
    def drive(self):        # 'self' represents the object that we are currently working with
                            # Giving 'self' as parameter is mandatory for a function defined inside a class (even if it does not take any other parameters)
        print(f"This {self.model} is driving")

    # Class Method 2 
    #################
    def stop(self):         # 'self' represents the object that we are currently working with
                            # Giving 'self' as parameter is mandatory for a function defined inside a class (even if it does not take any other parameters)
        print(f"This {self.model} has stopped.")
```

## Create another file `main.py` where we will `import` the `Car` class from `car.py` module and create objects of `class Car`.

## `main.py`

```py
# importing Car class from car module (car.py file)
from car import Car

# Creating an object of Car class
car_1 = Car("Chevy", "Corvette", 2021, "Blue")
car_2 = Car("Ford", "Mustang", 2022, "red")

# Printing the car_1 object attributes
print(car_1.make)
print(car_1.model)
print(car_1.year)
print(car_1.color)

# calling the 'Car' class methods on 'car_1' object 
car_1.drive()
car_1.stop()

print()

# Printing the car_2 object attributes
print(car_2.make)
print(car_2.model)
print(car_2.year)
print(car_2.color)

# calling the 'Car' class methods on 'car_1' object 
car_2.drive()
car_2.stop()


# Output:
# *******

# Chevy
# Corvette
# 2021
# Blue
# This Corvette is driving
# This Corvette has stopped.

# Ford
# Mustang
# 2022
# red
# This Mustang is driving
# This Mustang has stopped.
```
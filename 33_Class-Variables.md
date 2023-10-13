# `car.py`

```py
class Car:

    wheels = 4 # class variable

    # class variable is a variable/attribute - with a default value - that belongs to the class itself. 
    # The default value of the class variable for every object of the class is same.
    # However we can change the class variable value both
            # for a particular object
            # for the entire class

    def __init__(self, make, model, year, color):
        self.make = make        # instance variable
        self.model = model      # instance variable
        self.year = year        # instance variable
        self.color = color      # instance variable

    def drive(self):
        print(f"This {self.model} is driving")

    def stop(self):
        print(f"This {self.model} has stopped.")
```

# `main.py`

```py
from car import Car

car_1 = Car("Chevy","Corvette",2021,"blue")
car_2 = Car("Ford","Mustang",2022,"red")


# Car.wheels = 4        # class variable

# Changing the class variable 'wheels' value for car_1 object only
car_1.wheels = 3

print(car_1.wheels)     # 3
print(car_2.wheels)     # 4

# Changing the class variable 'wheels' value for the whole class 'Car' 
Car.wheels = 2

print(car_1.wheels)     # 3   # User-defined value > Default value   # car_1.wheels = 3
print(car_2.wheels)     # 2
```
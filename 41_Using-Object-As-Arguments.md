# Example 1:

```py
class Car:
    def __init__(self, maker, model, color):
        self.maker = maker
        self.model = model
        self.color = color
    
    def run():
        print("Car is running")

    def stop():
        print("Car has stopped")


# Creating a separate-independent method (outside Car class) for using the Car class objects.
def printDetails(carObject):
    print(f"The maker of this car is : {carObject.maker}")
    print(f"The model of this car is : {carObject.model}")
    print(f"The color of this car is : {carObject.color}")


# Creating Car class object
car_1 = Car("Hyundai", "i10", "red")

# Using car_1 object as an argument for method : printDetails(carObject)
printDetails(car_1)
# The maker of this car is : Hyundai
# The model of this car is : i10
# The color of this car is : red
```


# Example 2:

```py
class Car:
    color = None        # Class attribute

class Motorcycle:
    color = None        # Class Attribute

# Creating a separate-independent method (outside all classes) for using class objects.
def change_color(object,color):
    object.color = color


car_1 = Car()
car_2 = Car()
car_3 = Car()
bike_1 = Motorcycle()

change_color(car_1,"red")           # Using car_1 object as an argument  
change_color(car_2,"white")         # Using car_2 object as an argument
change_color(car_3,"blue")          # Using car_3 object as an argument
change_color(bike_1,"black")        # Using bike_1 object as an argument

print(car_1.color)      # red
print(car_2.color)      # white
print(car_3.color)      # blue
print(bike_1.color)     # black
```
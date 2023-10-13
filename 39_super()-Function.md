```py
# super() : is used to access the methods of a parent class.
#           Returns a temporary object of a parent class when used.

class Quadrilateral:

    def __init__(self, length, width):
        self.length = length
        self.width = width

class Rectangle(Quadrilateral):

    def __init__(self, length, width):
        super().__init__(length,width)              # Accessing the __init__() method of Parent class Quadrilateral
        
    def area(self):
        return self.length*self.width


class Cube(Rectangle):

    def __init__(self, length, width, height):
        super().__init__(length,width)              # Accessing the __init__() method of Parent class Rectangle
        self.height = height

    def volume(self):
        return self.length*self.width*self.height


rectangle = Rectangle(2,3)
print(rectangle.area())     # 6

cube = Cube(3, 3, 3)
print(cube.volume())        # 27
```
```py
# Method Chaining: Used to call multiple methods sequentially - on the same object.
#                  Each call performs an action on the same object and returns self.


class Car:

    def turn_on(self):
        print("You start the engine")
        return self                         # It is mandatory for those functions which are to be used for 
                                            # method chaining in future - to atleast return 'self'  

    def drive(self):
        print("You drive the car")
        return self                         # It is mandatory for those functions which are to be used  
                                            # for method chaining in future - to atleast return 'self'  

    def brake(self):
        print("You step on the brakes")
        return self                         # It is mandatory for those functions which are to be used  
                                            # for method chaining in future - to atleast return 'self'  

    def turn_off(self):
        print("You turn off the engine")
        return self                         # It is mandatory for those functions which are to be used  
                                            # for method chaining in future - to atleast return 'self'  


car = Car()

car.turn_on().drive().brake().turn_off()        # Method Chaining
# You start the engine
# You drive the car
# You step on the brakes
# You turn off the engine

# car.turn_on()\
#     .drive()\
#     .brake()\
#     .turn_off()                                 # This is another way of writing method chaining
#                                                 # '\' is called "Line Continuation Character"
```
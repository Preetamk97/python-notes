```py
# Duck Typing = It is a programming concept that says the class of an object is less important than 
#               the methods/attributes that this class may have.
# Class type is not checked if the required methods/attributes are present.

# Concept Demostration
#######################
class Duck:

    def walk(self):
        print("This duck is walking")

    def talk(self):
        print("This duck is qwuacking")

class Chicken:

    def walk(self):
        print("This chicken is walking")

    def talk(self):
        print("This chicken is clucking")


class Person():

    def catch(self, food):
        food.walk()
        food.talk()
        print("Caught todays food!")

duck = Duck()
chicken = Chicken()
person = Person()

person.catch(chicken)
# This chicken is walking
# This chicken is clucking     
# Caught todays food!
person.catch(duck)
# This duck is walking
# This duck is qwuacking
# Caught todays food!

# Like the person doesn't care what he catches (Chicken or Duck) for his dinner as long as the food is alive (it can walk and talk) and he can eat it -- In the same manner, Python Interpreter here doestn't really care here about "what Object of which Class" are you going to feed it as an argument for the method 'catch(self, food)' -- as long as this object's Class has these two methods [ walkl() & talk() ] available. Any type of object works as long as it can call these two methods - walkl() & talk() 

# This progreamming concept os simply named - Duck Typing
# “If it walks like a duck, and it quacks like a duck, then it must be a duck.”
```
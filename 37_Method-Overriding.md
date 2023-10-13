```py
# Method Overiding : It is a concept in Python OOP as per which we can provide a customized/overidden 
#                    defnition (that suits our need) for a method inside a child/derived class 
#                    - whose definition is already provided inside the parent class.

# Order of Priority: CHILD CLASS(overidden method) >> PARENT CLASS(original method)

class Animal:
    
    #overriden method
    def eat(self):
        print("This animal is eating")

class Rabbit(Animal):
    
    #overriding method
    def eat(self):
        print("This rabbit is eating a carrot")


rabbit = Rabbit()
rabbit.eat()        # This rabbit is eating a carrot

# Order of Priority: CHILD CLASS(overidden method) >> PARENT CLASS(original method)
```
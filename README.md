# third-try
cs.py
#Defining a list of names
names = ["Harry", "Ron", "Hermoine", "Ginny"]

# Append adds an element to the end of a list
names.append("Draco")

# .sort() will put the elements of the list in Alphabetical order
names.sort()
print(names)

# Creating sets, sets are unordered lists w/ unique elements( yani no element ever appears twice in a set)
s = set()
# .add() adds a new element
s.add(1)
s.add(4)
# .remove() aloowes you to remove an element
s.remove(1)

#How many elements are in an item/list/element? use len
len(s)
#using an f string to combine string and expressions/functions
print(f"This set has {len(s)} many elements")

#Learing to create a loop
#in this case making a counter
for i in [1, 2, 3,4 ]:
    print(i)
    #or you can use range() if you dont want to type every number (starts at 0)

for i in range(6):
    print(i)    

names = ["Harry", "Ron", "Hermoine", "Ginny"]
for name in names:
    print(name)

#Python dictinory dict
houses = {"Harry": "Gryffindor", "Draco": "Slytherin"}
# houses is the dict and Harry holds the value of Gryffindor
print(houses["Harry"]) #this would return Gryffindor

#FUNCTIONS in py
# def means define
# for exp we want the square of a number
def square(x):
    return x * x

for i in range(10):
    print(f"The square of {i} is {square(i)}")


# how to import functions for example my function is in file ex and the f you want is names square
from ex import square 
#OR
import ex 
for i in range(10):              #*   
    print(f"The square of {i} is {ex.square(i)}")

#~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
#classes (look up at mimo bop)
class Point():
    def __init__(self) -> None:
        pass

#decorators: a function that can serve as a value, you can use is at input/output in other functions aka. functional programming paradime
def announce(f):
    def wrapper():
        print("About to run function")
        f()
        print("Done!")
    return wrapper
    
@announce
def hello():
    print("Hi")


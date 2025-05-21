# EXP 27: Python OOP: Encapsulation with Private Members

##  AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.



##  ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.


##  Program
```
class Rectangle:
    def __init__(self,length,width):
        self.__length=length
        self.__width=width
    
    def display(self):
        print(self.__length) #displaying inside the class
        
obj=Rectangle(5,3)
obj.display()
print(obj._Rectangle__width) #displaying outside the class
```
## Output
![image](https://github.com/user-attachments/assets/d96d7b49-7842-4aa1-96b9-9874580b3d37)

## Result
Thus, the program is verified successfully.

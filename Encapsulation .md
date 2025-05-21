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
    def __init__(self, length, breadth):
        self.__length = length      
        self.__breadth = breadth    
        
        # Step 3: Print Values
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)

rect = Rectangle(10, 5)
```
## Output
![image](https://github.com/user-attachments/assets/47fd80b7-5a21-4119-9358-1139a313f346)

## Result
Thus, the program is verified successfully.

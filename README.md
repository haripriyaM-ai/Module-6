## MODULE - 6
# EXP 26: Python OOP: Abstract Class & Method Example

##  AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.


##  ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.


##  Program
```
from abc import ABC
class Shape(ABC): 
    def calculate_area(self):
      pass

class Rectangle(Shape):
  length = 6
  breadth = 4
  def calculate_area(self):
      return self.length*self.breadth

class Circle(Shape):
  radius = 7
  def calculate_area(self):
      return 3.14*self.radius*self.radius

r=Rectangle()
c=Circle() 

print("Area of a rectangle:", r.calculate_area()) 
print("Area of a circle:", c.calculate_area())  
```
## Output
![image](https://github.com/user-attachments/assets/af39e824-8e90-431a-b381-d8a6a03f86d7)

## Result
Thus, the program is verified successfully.

---

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

---

# EXP 28: Method Overriding-Fish and Shark Class Inheritance in Python

##  AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

##  ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
    def type(self):
        print("fish")   

class Shark(Fish):
	def type(self):
	    print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()


obj_goldfish.type()
obj_hammerhead.type()
```
## OUTPUT
![image](https://github.com/user-attachments/assets/e951d77c-b948-4b05-841c-9992acdb44f2)

## RESULT
Thus, the program is verified successfully.

---

# EXP 29: Python OOP: Operator Overloading (Less Than `<`)

##  AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.


##  ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.


##  Program
```
class A:
    def __init__(self,a):
        self.a=a
    def __lt__(self,o):
        return self.a < o.a
        
ob1=A(200)
ob2=A(30)

if(ob1<ob2):
    print("ob1 is less than ob2")
else:
    print("ob2 is less than ob1")
```
## Output
![image](https://github.com/user-attachments/assets/c7568781-1e12-4618-a34e-fb933c70e06e)

## Result
Thus, the program is verified successfully.

---

# EXP 30: Python OOP: Polymorphism with Classes

##  AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.


##  ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.


## Program
```
class Beans(): 
     def type(self): 
       print("Vegetable") 
     def color(self):
       print("Green") 
class Mango(): 
     def type(self): 
       print("Fruit") 
     def color(self): 
       print("Yellow")      
def func(obj): 
      obj.type() 
      obj.color()
obj_beans = Beans() 
obj_mango = Mango() 
func(obj_beans) 
func(obj_mango)
```
## Output
![image](https://github.com/user-attachments/assets/dcce8067-5080-4ef6-83da-3dd7eff86eba)

## Result
Thus, the program is verified successfully

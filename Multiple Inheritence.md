# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
# Parent class
class Parent:
    def __init__(self, name):
        self.name = name

    def getName(self):
        return self.name


# Child class
class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

    def getAge(self):
        return self.age


# Grandchild class
class Grandchild(Child):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location

    def getLocation(self):
        return self.location


# Main program
name = input("Enter name: ")
age = int(input("Enter age: "))
location = input("Enter location: ")

obj = Grandchild(name, age, location)

print("\nPerson Details")
print("Name:", obj.getName())
print("Age:", obj.getAge())
print("Location:", obj.getLocation())
```
## Output Example
```
Enter name: Arun
Enter age: 21
Enter location: Chennai

Person Details
Name: Arun
Age: 21
Location: Chennai
```
## RESULT
Thus the program ran successfully and output was verified

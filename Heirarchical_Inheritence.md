# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
# Base class
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def getName(self):
        return self.name

    def getAge(self):
        return self.age


# Derived class 1
class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age)
        self.employee_id = employee_id
        self.department = department

    def getEmployeeDetails(self):
        print("\nEmployee Details")
        print("Name:", self.getName())
        print("Age:", self.getAge())
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)


# Derived class 2
class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease

    def getPatientDetails(self):
        print("\nPatient Details")
        print("Name:", self.getName())
        print("Age:", self.getAge())
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)


# Main program
# Employee input
ename = input("Enter Employee Name: ")
eage = int(input("Enter Employee Age: "))
eid = input("Enter Employee ID: ")
edept = input("Enter Department: ")

emp = Employee(ename, eage, eid, edept)

# Patient input
pname = input("\nEnter Patient Name: ")
page = int(input("Enter Patient Age: "))
pid = input("Enter Patient ID: ")
disease = input("Enter Disease: ")

pat = Patient(pname, page, pid, disease)

# Display details
emp.getEmployeeDetails()
pat.getPatientDetails()
```
## Sample Output
```
Enter Employee Name: Ravi
Enter Employee Age: 30
Enter Employee ID: E101
Enter Department: IT

Enter Patient Name: Sita
Enter Patient Age: 25
Enter Patient ID: P202
Enter Disease: Fever

Employee Details
Name: Ravi
Age: 30
Employee ID: E101
Department: IT

Patient Details
Name: Sita
Age: 25
Patient ID: P202
Disease: Fever
```
## RESULT
Thus the program ran successfully and output was verified

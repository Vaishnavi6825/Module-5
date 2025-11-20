# Ex.No:5E Hierarchical Inheritance
# AIM
To write a Python program to get the employee and doctor details and display them using hierarchical inheritance. Create a parent (base) class named Details and two child (derived) classes named Employee and Doctor.

# ALGORITHM
Begin the program. Create a class Details with an init method to initialize three attributes: id, name, and gender. Define a method display_details() to print the values of id, name, and gender. Create a class Employee that inherits from the Details class. Add two additional attributes: company and department. Override the display_details() method to print the employee-specific attributes (company and department) along with the inherited details. Create a class Doctor that also inherits from the Details class. Add two additional attributes: hospital and department. Override the display_details() method to print the doctor-specific attributes (hospital and department) along with the inherited details. Accept input for employee and doctor details. Create objects of Employee and Doctor using the input. Call the display_details() method for both objects to print the details. Terminate the program.

# PROGRAM
~~~
Reg-212222060245 Name- Singamala Rakshitha
# hierarchical inheritance

class Details:
    def __init__(self):
        self.__id="<No Id>"
        self.__name="<No Name>"
        self.__gender="<No Gender>"
    def setData(self,id,name,gender):
        self.__id=id
        self.__name=name
        self.__gender=gender
    def showData(self):
        print("Id: ",self.__id)
        print("Name: ", self.__name)
        print("Gender: ", self.__gender)

class Employee(Details): #Inheritance
    def __init__(self):
        self.__company="<No Company>"
        self.__dept="<No Dept>"
    def setEmployee(self,id,name,gender,comp,dept):
        self.setData(id,name,gender)
        self.__company=comp
        self.__dept=dept
    def showEmployee(self):
        self.showData()
        print("Hospital: ", self.__company)
        print("Department: ", self.__dept)

class Patient(Details): #Inheritance
    def __init__(self):
        self.__hospital="<No Hospital>"
        self.__dept="<No Dept>"
    def setEmployee(self,id,name,gender,hos,dept):
        self.setData(id,name,gender)
        self.__hospital=hos
        self.__dept=dept
    def showEmployee(self):
        self.showData()
        print("Hospital: ", self.__hospital)
        print("Department: ", self.__dept)

id=int(input())
name=input()
gender=input()
comp=input()
dept=input()
id1=int(input())
nam=input()
gen=input()
hosp=input()
dep=input()

print("Doctor Object")
e=Employee()
e.setEmployee(id,name,gender,comp,dept)
e.showEmployee()
print("\nPatient Object")
d = Patient()
d.setEmployee(id1, nam, gen, hosp, dep)
d.showEmployee()
~~~
# OUTPUT
<img width="1183" height="465" alt="image" src="https://github.com/user-attachments/assets/c4b3a3d7-e289-44fa-878e-3e058a797343" />

# RESULT 
Thus the program to get the employee and doctor details and display them using hierarchical inheritance has been implemented and executed successfully.

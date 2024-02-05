# -practice-question-on-classes-and-objects-in-Python
Certainly! Here's another practice question on classes and objects in Python:

Practice Question:

You are building a program to manage student information for a school. Define a class `Student` to represent a student's information.

The `Student` class should have the following attributes and methods:
- Attributes:
  - `name` (string): representing the name of the student.
  - `roll_number` (string): representing the unique roll number of the student.
  - `marks` (list of integers): representing the marks obtained by the student in different subjects.
- Methods:
  - `__init__(self, name, roll_number)`: constructor to initialize the attributes `name` and `roll_number`. Initialize `marks` as an empty list.
  - `add_marks(self, subject, marks)`: method to add the marks obtained by the student in a subject to the `marks` list.
  - `calculate_total_marks(self)`: method to calculate and return the total marks obtained by the student.
  - `display_info(self)`: method to display the information of the student (name, roll number, and total marks obtained).

Create an instance of the `Student` class, add marks for different subjects, calculate the total marks, and display the student's information.

Solution:

```python
class Student:
    def __init__(self, name, roll_number):
        self.name = name
        self.roll_number = roll_number
        self.marks = []
    
    def add_marks(self, subject, marks):
        self.marks.append((subject, marks))
        print(f"Added marks for {subject}: {marks}")
    
    def calculate_total_marks(self):
        total_marks = sum(marks for subject, marks in self.marks)
        return total_marks
    
    def display_info(self):
        print(f"Name: {self.name}")
        print(f"Roll Number: {self.roll_number}")
        print(f"Total Marks Obtained: {self.calculate_total_marks()}")

# Create an instance of Student
student1 = Student("John Doe", "12345")

# Add marks for different subjects
student1.add_marks("Math", 90)
student1.add_marks("Science", 85)
student1.add_marks("English", 88)

# Display student's information
student1.display_info()
```

Explanation:

- The `Student` class is defined with attributes `name`, `roll_number`, and `marks`, along with methods `add_marks`, `calculate_total_marks`, and `display_info`.
- The `__init__` method initializes the name and roll number of the student and initializes `marks` as an empty list.
- The `add_marks` method adds the marks obtained by the student in a subject to the `marks` list along with the subject name.
- The `calculate_total_marks` method calculates the total marks obtained by the student by summing up the marks in all subjects.
- The `display_info` method displays the information of the student including name, roll number, and total marks obtained.
- An instance of the `Student` class (`student1`) is created with the name "John Doe" and roll number "12345".
- Marks for different subjects are added using the `add_marks` method.
- The student's information is displayed using the `display_info` method, which also calculates and displays the total marks obtained by the student.

PROJECT OVERVIEW

This is a project has 6 parts which are Section A, Section B, Section C, Section D, Section E and Section F.
The program allows users to enter student information such as their names, grades and subjects.
The tool used for this system is pyCharm.
It can perform other functions such as calculating student average and class average.
Its purpose is to allow users to see the display of student records for future references.

SETUP INSTRUCTIONS

It shows one how to run the program.
1. Open the project file in PyCharm
2. Select the desired section either Section A.py or Section B.py
3. Right-click the file and select run.
4. Input the input in the terminal
5. Look at the output displayed.

FEATURES LIST

This shows the list what the program can perform.
1. Allowing students to enter information
2. Calculating averages for student grades.
3. Displays results of student information.
4. Validating student grades entered.
5. Adding student grades.
6. Creating a class design with student objects.
7. Using advanced operations such as adding, removing and searching for students by average or grade.
8. Using comprehensive Testing to ensure that it is thorougly tested.
9. Searching and sorting algorithms.

CLASS ARCHITECTURE

This is a simple diagram that explains the classes in the program and how they relate to each other.
However, in my program I used lists, tuples, loops, variables and I did not include any classes, so there is no class architecture in this stage.

Section A:
-Stores student names and grades in lists.
-Calculates class average.
-Displays student names and their grades.
-Displays class average.

Section B:
- Uses a list of subjects and stores in each student name.
- It calculates averages for each student.
- It displays the highest and lowest values.

Section C:
-replaces list of tuples in a dictionary
-adds a new student to the tuple
-updates an existing student grades
-printing dictionary values.

Section D:
1.creating functions for:
-adding students
-calculating average.
-displaying student 
-displaying students summary

2. Searching and updating students.

3. Error handling:
-non-numeric grade input and missing data.
-providing informative error messages

SECTION E:
Transitioning to Object-Oriented Programming
1. Class Design:
-Creating Student Class with attributes student's name, grades and mthods to add grades, calculate the average and print the student details.
-Develop a GradeBook that contains a collection of student objects and provides methods to manage student records.

2. Advanced Operations:
-Implementing methods in the gradebook class to add, remove, and search for students.
-Includes sorting students by their average grade.

3.Comprehensive testing:
-ensuring that system is thoroughly tested including unit tests for individual methods.

SECTION F
Works on Execption Handling and Final Enhancements.
1. Exception Handling
- e.g StudentNotFoundError

2. Searching and Sorting:

3. Edge Cases to Handle

Class Architecture (Textual Description)

The system uses two main classes, Student and Gradebook, plus a set of custom exception classes. 
Section E introduced the two main classes. Student and GrdaeBook
Section F added the exceptions and extended Gradebook with searching and sorting.

STUDENT
A student object represents one student. Its stores the student name and dictionary of grades. with one list for each subject.(Math, English and Science.)
It is responsible for its own data. It can add a grade to a subject, calculate the average for one subject, calculate the overall average, and print its own details.
Every grade is checked before it is stored.

GRADEBOOK
A Gradebook object manages the whole class. It has a list of Student objects and provides the operations that work for students:
Managing students: adding a student it also rejects empty and duplicate names, and removing a student.
Searching: finding a student by exact name, finding by part of a name, and a version of the exact search that raises an error if the student is missing. Name matching ignores upper and lower case.
Grades: adding a grade to a student and updating an existing grade. If an update is invalid, the old grade is kept.
Sorting: sorting students by name, by overall average, or by their average in one subject. Sorting returns a new list, so the original order is never changed.
Display: printing the details of all students or of a given list.

RELATIONSHIP BETWEEN CLASSES 
Gradebook and Student have a one-to-many composition relationship. One Gradebook contains many Student objects, and the gradebook creates, finds and removes them. A Student does not know about the gradebook.
When a grade is added through the gradebook, it first finds the correct student and then asks that Student to store the grade. This keeps each class focused on one job: Student handles the data for one person, and Gradebook handles the collection.


INPUT/OUTPUT

shows screenshots of input and output statements in the terminal when running the program.

Section A: Prints the student names and their grades as well as the class average.
<img width="1920" height="1080" alt="Screenshot (348)" src="https://github.com/user-attachments/assets/282037d7-643b-4b4e-b96f-e6f137df8bb8" />


Section B: Prints student name, their grade and their average.
<img width="1920" height="1080" alt="Screenshot (349)" src="https://github.com/user-attachments/assets/58fe3da8-ad54-44b5-b84e-51ecfb1a5fc8" />



Section C: Implements a feature to search for a specific student by name and retrieving their grades and average
<img width="1920" height="1080" alt="Screenshot (350)" src="https://github.com/user-attachments/assets/77b7262c-74ca-45a9-b549-359435cfcc96" />

<img width="1920" height="1080" alt="Screenshot (351)" src="https://github.com/user-attachments/assets/5828d10a-fe8e-4ab3-a5c9-c956e67794e2" />

Section D: Shows a summary table of students names along with their grades, averages and class averages, including those of the added student.

Section E: Classes and objects
<img width="1920" height="1080" alt="Screenshot (543)" src="https://github.com/user-attachments/assets/c4147fe8-b892-4836-b6eb-d5b02c638dc9" />

Section F
<img width="1920" height="1080" alt="Screenshot (544)" src="https://github.com/user-attachments/assets/72e9eecd-4832-4028-931a-454ae9ce4510" />





ASSUMPTIONS AND LIMITATIONS

ASSUMPTIONS:
Section A-C:
1. The number of students must be a whole number.
2. The grades must be any value between 0 and 100.

Section D:
1. The user must add a name that does not exist in the system.
2. The student name can only be a string
3. The class and the student average must be displayed.

LIMITATIONS:
Section A-C
1. The program does not permanently store student information.

Section D:
1.Everything lives in the subject dictionary in memory, so when the program ends, anything you added or updated (like Khloe) is lost.

TESTING SUMMARY

This is the stage of testing your program by running it.
You enter different inputs and view the results.
The value entered can be invalid and programs denies user from proceeding.


| SECTION | TEST TO CARRY OUT           | WHAT TO EXPECT          | WHAT HAPPENED                     | RESULT |
|---------|-----------------------------|-------------------------|-----------------------------------|--------|
| A       | Correct Input               | Input accepted          | Grades were accepted              | Pass   |
| B       | Search for existing student | Grades displayed        | Grades were displayed             | Pass   |
| C       | Test Feature                | Expected output         | Expected output was produced      | Pass   |
| D       | Modularization of functions | Adding new student name | Entering name that already exists | Fail   |
| E + F   | Creating classes            | Name and Grade          | Invalid name                      | Fail   |


KNOWN ISSUES

Section A: had an issue in line 13.
The grade validation was written as 'and'. instead of 'or'. A number can either be below 0 number or above 100, can never be at the same time.

Section B: an issue was discovered in line 39, whereby student_average variable was not entered correctly.
The issue was resolved by entering the correct variable 'student_average' instead of 'average'.

Section D: The brief says each function should have a clear purpose and be reusable. A few of mine mix asking for input with doing the work. This can be resovled by using the main menu feature.

REFERENCES
This work is referenced from Introduction to python programming notes and a website https://www.iimchyderabad.com/Material/introduction-to-python-programming.pdf 

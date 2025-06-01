# University Database  

The University Database is a database design problem from the book [Database System Concepts](https://db-book.com/) authored by Abraham Silberschatz, Henry Korth, and S. Sudarshan, published by McGraw-Hill Education. This problem is commonly used in database courses to teach normalization, SQL queries, and schema design.

This problem involves creating a schema to manage information about students, instructors, courses, departments, and course enrollments. The database should track which courses are taught by which instructors in which semesters, which students take those courses, and the grades they receive.

## Entities, attributes, and relationships

- **Student**: The student entity represents the students enrolled in the university. Each student has the following attributes:
    - `name`: The name of the student.
    - `total credits`: The total number of credits the student has earned.

- **Instructor**: The instructor entity represents the instructors teaching courses at the university. Each instructor has the following attributes:
    - `name`: The name of the instructor.
    - `salary`: The salary of the instructor.

- **Department**: The department entity represents the academic departments in the university. Each department has the following attributes:
    - `department name`: The name of the department (primary key).
    - `building`: The building where the department is located.
    - `budget`: The budget allocated to the department.

- **Course**: The course entity represents the courses offered by the university. Each course has the following attributes:
    - `title`: The title of the course.
    - `credits`: The number of credits the course is worth.

- **Section**: The section entity represents a specific offering of a course in a given semester and year. Each section has the following attributes:
    - `semester`: The semester in which the section is offered (e.g., "Fall", "Spring").
    - `year`: The year in which the section is offered.
    - `building`: The building where the section is held.
    - `room number`: The room number where the section is held.
    - `time slot`: The time slot during which the section meets:
        - `day`: The day(s) of the week the section meets (e.g., "Monday", "Wednesday").
        - `start time`: The start time of the section.
        - `end time`: The end time of the section.

- **Classroom**: The classroom entity represents the physical classrooms where sections are held. Each classroom has the following attributes:
    - `building`: The building where the classroom is located.
    - `room number`: The room number of the classroom.
    - `capacity`: The maximum number of students that can be accommodated in the classroom.


Beyond the entities and attributes, you have also identified the following relationships:

- A **Student** belongs to a **Department**.
- An **Instructor** belongs to a **Department**.
- A **Course** belongs to a **Department**. 
- A course may have a prerequisite course, which is also a **Course**. A course can also be a prerequisite for another course.
- A **Section** is an offering of a **Course** in a specific semester/year. A specific semester/year can have multiple sections of the same course.
- A **Teacher** can teach multiple **Sections** of the same or different courses in a semester/year. A **Section** is taught by only one **Instructor**.
- A **Student** can take multiple **Sections** in a semester/year, and a **Section** can have multiple **Students** enrolled.
- A **Student** can receive a **grade** for each **Section** they take
- A **Student** has only one **Advisor** (an **Instructor**). An **Instructor** can advise multiple **Students**.
- A **Section** occurs in a **Classroom** and is assigned a time slot. A specific **Classroom** can be used for only one **Section** at a time.

## Constraints and other information

- Each time slot can include multiple day entries (e.g., 9:00 AM - 10:30 AM on Monday and Wednesday).
- The grade of a student for a section can be NULL when the course is still ongoing.

## 📂 Usage

## Solution sample

A sample design of the database for the university system from the book [Database System Concepts](https://db-book.com/) can be found [here](samples/university-system-sample.png). The sample adopts the Chen's Notation. Another sample design using the Crow's Foot Notation will be available soon.
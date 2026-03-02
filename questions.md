# Question 1 - Exam Style Questions.

1.	Identify two entities shown in the database diagram and briefly describe what real-world objects they represent. [4]

Student table: Represents individual students in reality, storing personal information such as student ID, name, date of birth, email, and year of enrollment.
Department table: Represents academic departments in a school (such as the Department of Computer Science, Department of Mathematics), storing department IDs and department names.

2.	Define the term primary key with reference to one primary key from the database. [2]

The primary key is the field in a table that uniquely identifies each record. For example, StudentId in the Student table is the primary key, ensuring the uniqueness of each student record.

3.	Explain what is meant by a foreign key. Using the database diagram, identify one foreign key and describe the relationship it enforces. [3]

A foreign key is a field used to establish relationships between tables. For example, the DepartmentId in the Course table is a foreign key that references the DepartmentId in the Department table, enforcing the one-to-many relationship where "one department can offer multiple courses".

4.	Describe how the database models the relationship between students and courses. Explain why this relationship cannot be represented using a single table. [3]

The relationship between students and courses is many-to-many (a student can select multiple courses, and a course can be selected by multiple students). This relationship needs to be implemented through the Enrolment table as an intermediary table, as a single table cannot store cross-reference information between students and courses simultaneously.

5.	Explain the purpose of the Enrolment table. Identify two attributes stored in this table and justify why they belong there rather than in another table. [4]

Function: Record specific information about students' course selection, including academic year, semester, and grades.
Attribute example:
StudentId: It is associated with students and represents an enrollment behavior rather than an inherent attribute of students. It should be stored in the Enrolment table.
AcademicYear: Records the academic year of course selection, which is a temporal attribute of the course selection event and does not belong to the student or the curriculum schedule.

6.	Identify the highest normal form that this database satisfies and justify your answer with reference to the structure of the tables and their attributes. [4]

This database satisfies the third normal form (3NF):
All tables have primary keys, and non-primary key fields are completely dependent on the primary key without any transitive dependencies. Tables are explicitly associated through foreign keys, with no duplicate data storage.


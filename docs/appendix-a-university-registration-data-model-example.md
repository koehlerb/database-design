---
sidebar_label: 'Appendix A University Registration Data Model Example'
sidebar_position: 20
---

# Appendix A University Registration Data Model Example

Here is a statement of the data requirements for a product to support 
the registration of and provide
  help to students of a fictitious e-learning university.

An e-learning university needs to keep details of its students and staff, 
the courses that it offers and
  the performance of the students who study its courses. The university 
  is administered in four
  geographical regions (England, Scotland, Wales and Northern Ireland).

Information about each student should be initially recorded at registration. 
This includes the student’s
  identification number issued at the time, name, year of registration and 
  the region in which the student
  is located. A student is not required to enroll in any courses at 
  registration; enrollment in a course
  can happen at a later time.

Information recorded for each member of the tutorial and counseling staff 
must include the staff number,
  name and region in which he or she is located. Each staff member may act as 
  a counselor to one or more
  students, and may act as a tutor to one or more students on one or 
  more courses. It may be the case
  that, at any particular point in time, a member of staff may not be 
  allocated any students to tutor or
  counsel.

Each student has one counselor, allocated at registration, who supports 
the student throughout his or her
  university career. A student is allocated a separate tutor for each course 
  in which he or she is
  enrolled. A staff member may only counsel or tutor a student who is resident 
  in the same region as that
  staff member.

Each course that is available for study must have a course code, a title and 
a value in terms of credit
  points. A course is either a 15-point course or a 30-point course. A course 
  may have a quota for the
  number of students enrolled in it at any one presentation. A course 
  need not have any students
  enrolled in it (such as a course that has just been written and offered 
  for study).

Students are constrained in the number of courses they can be enrolled in at 
any one time. They may not
  take courses simultaneously if their combined points total exceeds 180 points.

For assessment purposes, a 15-point course may have up to three assignments 
per presentation and a
  30-point course may have up to five assignments per presentation. The grade 
  for an assignment on any
  course is recorded as a mark out of 100.

The university database below is one possible data model that describes the 
above set of requirements.
  The model has several parts, beginning with an ERD and followed by a 
  written description of entity
  types, constraints, and assumptions.

## Design Process

See Figure A.1.

1. The first step is to determine the kernels. These are typically nouns: 
    Staff, Course, Student and
    Assignment.
1. The next step is to document all attributes for each entity. This is where 
    you need to ensure that
    all tables are properly normalized.
1. Create the initial ERD and review it with the users.
1. Make changes if needed after the ERD review.
1. Verify the ER model with users to finalize the design.

![a data model for a student and staff records system](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-14-University-Example-ERD-300x189.jpg)

*Figure A.1. University ERD. A data model for a
    student and staff records system by A. Watt.*

### Entity

Student (<u>StudentID</u>, Name, Registered, Region, StaffNo)


Staff (<u>StaffNo</u>, Name, Region) – This table contains
  instructors and other staff members.

Course (<u>CourseCode</u>, Title, Credit, Quota, StaffNo)

Enrollment (<u>StudentlD, CourseCode</u>, DateEnrolled,
  FinalGrade)

Assignment (<u>StudentID, CourseCode, AssignmentNo</u>,
  Grade)

### Constraints

* A staff member may only tutor or counsel students who are located in the 
    same region as the staff
    member.
* Students may not enroll for more than 180 points worth of courses at any 
    one time.
* The attribute Credit (of Course) has a value of 15 or 30 points.
* A 30-point course may have up to five assignments; a 15-point course may 
    have up to three
    assignments.
* The attribute Grade (of Assignment) has a value that is a mark out of 100.

### Assumptions

* A student has at most one enrollment in a course as only current 
    enrollments are recorded.
* An assignment may be submitted only once.

### Relationships (includes cardinality)

Using Figure A.2, note that a student (record) is associated with (enrolled) 
with a minimum of 1 to a
  maximum of many courses.

Each enrollment must have a valid student.

<strong>Note:</strong>  Since the StudentID is part of the PK, it can’t be 
null. Therefore, any
  StudentID entered, must exist in the Student table at least once to a 
  maximum of 1 time. This
  should be obvious since the PK cannot have duplicates.

![student one to many enrollment](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-14-Student-one-to-Many-Enrollment-300x145.jpg)

*Figure A.2 by A. Watt.*

Refer to Figure A.3. A staff record (a tutor) is associated with a minimum of 
0 students to a maximum of
  many students.

A student record may or may not have a tutor.

![staff to student relationship](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-14-Staff-to-Student-300x174.jpg)

*Figure A.3 by A. Watt.*

<strong>Note:</strong>  The StaffNo field in the Student table
  allows null values – represented by the 0 on the left side.  However, 
  if a StaffNo exists in the
  student table it must exist in the Staff table maximum once – represented 
  by the 1.

Refer to Figure A.4. A staff record (instructor) is associated with a minimum 
of 0 courses to a
  maximum of many courses.

A course may or may not be associated with an instructor.

<strong>Note:</strong>  The StaffNo in the Course table is the FK, and it can 
be null. This
  represents the 0 on the left side of the relationship. If the StaffNo has 
  data, it has to be in the
  Staff table a maximum of once. That is represented by the 1 on the left side 
  of the relationship.

![staff to course relationship](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-14-Staff-to-Course-300x172.jpg)

*Figure A.4 by A. Watt.*

Refer to Figure A.5. A course must be offered (in enrollment) at least once to 
a maximum of many
  times.

The Enrollment table must contain at least 1 valid course to a maximum of many.

![course to enrollment relationship](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-14-Course-to-Enrollment-300x138.jpg)

*Figure A.5 by A. Watt.*

Refer to Figure A.6. An enrollment can have a minimum of 0 assignments or 
a maximum of many.

An assignment must be associated with at least 1 with a maximum of 1 enrollment.

<strong>Note:</strong>  Every record in the Assignment table must contain a 
valid enrollment record.
  One enrollment record can be associated with multiple assignments.

![enrollment to assignment relationship](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-14-Enrollment-to-Assignment-300x118.jpg)

*Figure A.6 by A. Watt.*

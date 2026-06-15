# DATABASE_RELATIONSHIPS.md

# EduNexus Database Relationships

## Overview

This document defines all relationships between tables in EduNexus.

Relationship Types:

* One-to-One (1:1)
* One-to-Many (1:N)
* Many-to-Many (M:N)

The design follows Third Normal Form (3NF) to minimize data duplication and maximize scalability.

---

# CORE FOUNDATION MODULE

## schools → users

Relationship Type:
One-to-Many (1:N)

Explanation:

One school can have many users.

Examples:

* Principal
* Deputy Principal
* Teachers
* Students
* Parents
* Librarians
* Bursars

Foreign Key:

users.school_id → schools.school_id

---

## users → user_roles

Relationship Type:
One-to-Many (1:N)

Explanation:

One user can hold multiple roles.

Examples:

Teacher John may also be:

* Teacher
* Club Patron
* Hostel Master

Foreign Key:

user_roles.user_id → users.user_id

---

## roles → user_roles

Relationship Type:
One-to-Many (1:N)

Explanation:

One role can be assigned to many users.

Examples:

Teacher Role

* John
* Mary
* Peter

Foreign Key:

user_roles.role_id → roles.role_id

---

## roles → role_permissions

Relationship Type:
One-to-Many (1:N)

Explanation:

One role can have many permissions.

Foreign Key:

role_permissions.role_id → roles.role_id

---

## permissions → role_permissions

Relationship Type:
One-to-Many (1:N)

Explanation:

One permission may belong to multiple roles.

Examples:

VIEW_STUDENTS

* Principal
* Deputy Principal
* Teacher

Foreign Key:

role_permissions.permission_id → permissions.permission_id

---

# STUDENT INFORMATION SYSTEM

## users → students

Relationship Type:
One-to-One (1:1)

Explanation:

Every student is a user.

Foreign Key:

students.user_id → users.user_id

---

## users → parents

Relationship Type:
One-to-One (1:1)

Explanation:

Every parent is a user.

Foreign Key:

parents.user_id → users.user_id

---

## users → staff

Relationship Type:
One-to-One (1:1)

Explanation:

Every staff member is a user.

Foreign Key:

staff.user_id → users.user_id

---

## students ↔ parents

Relationship Type:
Many-to-Many (M:N)

Implemented Through:

student_parents

Explanation:

One student can have multiple parents.

One parent can have multiple children.

Examples:

Student A

* Mother
* Father
* Guardian

Parent B

* Child A
* Child B

Foreign Keys:

student_parents.student_id → students.student_id

student_parents.parent_id → parents.parent_id

---

# ACADEMIC MODULE

## departments → staff

Relationship Type:
One-to-Many (1:N)

Explanation:

One department can have many teachers.

Examples:

Science Department

* Physics Teacher
* Biology Teacher
* Chemistry Teacher

Foreign Key:

staff.department_id → departments.department_id

---

## departments → subjects

Relationship Type:
One-to-Many (1:N)

Explanation:

One department can offer many subjects.

Examples:

Science Department

* Biology
* Chemistry
* Physics

Foreign Key:

subjects.department_id → departments.department_id

---

## staff → classes

Relationship Type:
One-to-Many (1:N)

Explanation:

One teacher may serve as class teacher for multiple classes.

Foreign Key:

classes.class_teacher_id → staff.staff_id

---

## classes → students

Relationship Type:
One-to-Many (1:N)

Explanation:

One class contains many students.

Foreign Key:

students.current_class_id → classes.class_id

---

## staff ↔ subjects

Relationship Type:
Many-to-Many (M:N)

Implemented Through:

teacher_subjects

Explanation:

One teacher may teach many subjects.

One subject may be taught by many teachers.

Examples:

Teacher John

* Mathematics
* Physics

Mathematics

* John
* Mary

Foreign Keys:

teacher_subjects.staff_id → staff.staff_id

teacher_subjects.subject_id → subjects.subject_id

---

# ATTENDANCE MODULE

## students → attendance

Relationship Type:
One-to-Many (1:N)

Explanation:

One student can have many attendance records.

Foreign Key:

attendance.student_id → students.student_id

---

## classes → attendance

Relationship Type:
One-to-Many (1:N)

Explanation:

One class can generate many attendance records.

Foreign Key:

attendance.class_id → classes.class_id

---

## staff → attendance

Relationship Type:
One-to-Many (1:N)

Explanation:

Teachers record attendance.

Foreign Key:

attendance.recorded_by → staff.staff_id

---

# LIBRARY MODULE

## books → book_loans

Relationship Type:
One-to-Many (1:N)

Explanation:

One book can be loaned many times.

Foreign Key:

book_loans.book_id → books.book_id

---

## students → book_loans

Relationship Type:
One-to-Many (1:N)

Explanation:

One student can borrow many books.

Foreign Key:

book_loans.student_id → students.student_id

---

## staff → book_loans

Relationship Type:
One-to-Many (1:N)

Explanation:

Librarians issue books.

Foreign Key:

book_loans.issued_by → staff.staff_id

---

# FINANCE MODULE

## classes → fee_structures

Relationship Type:
One-to-Many (1:N)

Explanation:

Each class can have multiple yearly fee structures.

Foreign Key:

fee_structures.class_id → classes.class_id

---

## students → payments

Relationship Type:
One-to-Many (1:N)

Explanation:

Students can make multiple payments.

Foreign Key:

payments.student_id → students.student_id

---

# COMMUNICATION MODULE

## conversations → messages

Relationship Type:
One-to-Many (1:N)

Explanation:

A conversation contains many messages.

Foreign Key:

messages.conversation_id → conversations.conversation_id

---

## users → messages

Relationship Type:
One-to-Many (1:N)

Explanation:

Users send messages.

Foreign Key:

messages.sender_id → users.user_id

---

# HOSTEL MODULE

## hostels → rooms

Relationship Type:
One-to-Many (1:N)

Explanation:

One hostel contains many rooms.

Foreign Key:

rooms.hostel_id → hostels.hostel_id

---

## students ↔ rooms

Relationship Type:
Many-to-Many Over Time

Implemented Through:

room_assignments

Explanation:

Students may move rooms over time.

Foreign Keys:

room_assignments.student_id → students.student_id

room_assignments.room_id → rooms.room_id

---

# CLUBS & ACTIVITIES

## staff → clubs

Relationship Type:
One-to-Many (1:N)

Explanation:

One staff member can patron multiple clubs.

Foreign Key:

clubs.patron_id → staff.staff_id

---

## students ↔ clubs

Relationship Type:
Many-to-Many (M:N)

Implemented Through:

club_memberships

Explanation:

Students may join multiple clubs.

Clubs contain many students.

Foreign Keys:

club_memberships.student_id → students.student_id

club_memberships.club_id → clubs.club_id

---

# OPPORTUNET MODULE

## opportunities → applications

Relationship Type:
One-to-Many (1:N)

Explanation:

One opportunity can receive many applications.

Foreign Key:

applications.opportunity_id → opportunities.opportunity_id

---

## students → applications

Relationship Type:
One-to-Many (1:N)

Explanation:

One student can apply to many opportunities.

Foreign Key:

applications.student_id → students.student_id

---

# AI MODULE

## users → ai_interactions

Relationship Type:
One-to-Many (1:N)

Explanation:

One user can have many AI conversations.

Foreign Key:

ai_interactions.user_id → users.user_id

---

# FUTURE IMPROVEMENTS

Recommended future normalization:

1. student_classes

Purpose:
Maintain student class history by academic year.

2. academic_terms

Purpose:
Term 1, Term 2, Term 3 management.

3. examinations

Purpose:
Exam definitions.

4. exam_results

Purpose:
Student performance records.

5. inventory

Purpose:
School asset management.

6. health_records

Purpose:
Student medical information.

7. transport

Purpose:
School transportation management.

8. video_conferencing

Purpose:
Online classes and meetings.

---

Version: 1.0

Project: EduNexus

License: Proprietary (All Rights Reserved)

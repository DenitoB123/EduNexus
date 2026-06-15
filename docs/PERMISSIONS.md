# PERMISSIONS.md

## Overview

EduNexus uses a Role-Based Access Control (RBAC) system.

Roles define WHO a user is.

Permissions define WHAT a user can do.

A role can have many permissions.

A permission can be assigned to many roles.

Example:

Teacher

* view_students
* record_attendance
* enter_grades

Principal

* all teacher permissions
* manage_staff
* view_reports

---

# User Management Permissions

## manage_users

Create, update, deactivate, and reactivate user accounts.

Assigned To:

* ICT Administrator
* Principal
* Director

---

## view_users

View user accounts.

Assigned To:

* Principal
* Deputy Principal
* ICT Administrator

---

## assign_roles

Assign roles to users.

Assigned To:

* ICT Administrator
* Principal

---

# Student Management Permissions

## create_students

Register new students.

Assigned To:

* Registrar
* Principal

---

## edit_students

Modify student information.

Assigned To:

* Registrar
* Principal

---

## view_students

View student records.

Assigned To:

* Teachers
* Parents
* Principal
* Deputy Principal

---

## delete_students

Remove student records.

Assigned To:

* Principal
* Director

---

# Parent Management Permissions

## create_parents

Register parent or guardian accounts.

Assigned To:

* Registrar

---

## edit_parents

Update parent information.

Assigned To:

* Registrar

---

## view_parents

View parent information.

Assigned To:

* Teachers
* Registrar
* Principal

---

# Staff Management Permissions

## create_staff

Register staff members.

Assigned To:

* Principal
* ICT Administrator

---

## edit_staff

Modify staff records.

Assigned To:

* Principal
* ICT Administrator

---

## view_staff

View staff records.

Assigned To:

* Principal
* Deputy Principal

---

# Academic Permissions

## manage_classes

Create and manage classes.

Assigned To:

* Principal
* Deputy Principal
* Registrar

---

## manage_subjects

Create and manage subjects.

Assigned To:

* Principal
* Head of Department

---

## enter_grades

Record examination and assignment marks.

Assigned To:

* Teacher

---

## edit_grades

Modify grades.

Assigned To:

* Teacher
* Head of Department

---

## publish_results

Release examination results.

Assigned To:

* Principal
* Deputy Principal

---

## view_results

View examination results.

Assigned To:

* Students
* Parents
* Teachers

---

# Attendance Permissions

## record_attendance

Record attendance.

Assigned To:

* Teacher
* Class Teacher

---

## edit_attendance

Modify attendance records.

Assigned To:

* Class Teacher
* Principal

---

## view_attendance

View attendance reports.

Assigned To:

* Teachers
* Parents
* Students
* Principal

---

# Communication Permissions

## send_messages

Send messages within EduNexus.

Assigned To:

* Teachers
* Students
* Parents
* Administrators

---

## create_groups

Create communication groups.

Assigned To:

* Teachers
* Administrators

---

## broadcast_announcements

Send school-wide announcements.

Assigned To:

* Principal
* Deputy Principal

---

# Library Permissions

## manage_books

Add and update books.

Assigned To:

* Librarian

---

## issue_books

Issue books to students.

Assigned To:

* Librarian

---

## receive_books

Receive returned books.

Assigned To:

* Librarian

---

## view_library_reports

View library statistics.

Assigned To:

* Librarian
* Principal

---

# Finance Permissions

## manage_fees

Create fee structures.

Assigned To:

* Bursar

---

## record_payments

Record school payments.

Assigned To:

* Bursar
* Accounts Clerk

---

## view_financial_reports

View financial reports.

Assigned To:

* Bursar
* Principal

---

## manage_payment_integrations

Manage M-Pesa and banking integrations.

Assigned To:

* ICT Administrator
* Bursar

---

# Hostel Permissions

## manage_hostels

Manage hostels and dormitories.

Assigned To:

* Hostel Master
* Hostel Mistress

---

## assign_rooms

Assign students to rooms.

Assigned To:

* Hostel Master
* Hostel Mistress

---

## view_hostel_reports

View hostel statistics.

Assigned To:

* Hostel Master
* Principal

---

# Clubs & Activities Permissions

## manage_clubs

Create and manage clubs.

Assigned To:

* Club Patron

---

## manage_events

Create and manage events.

Assigned To:

* Club Patron
* Sports Master
* Sports Mistress

---

# Inventory Permissions

## manage_inventory

Manage school inventory.

Assigned To:

* Storekeeper

---

## view_inventory

View inventory records.

Assigned To:

* Principal
* Storekeeper

---

# Opportunity Platform Permissions

## view_opportunities

View scholarships, competitions, internships, and programs.

Assigned To:

* Students
* Teachers

---

## publish_opportunities

Publish opportunities.

Assigned To:

* Administrators

---

## manage_opportunities

Manage opportunity database.

Assigned To:

* Administrators

---

# AI Permissions

## use_ai_assistant

Access EduNexus AI features.

Assigned To:

* Students
* Teachers
* Parents
* Administrators

---

## generate_ai_reports

Generate AI-powered reports.

Assigned To:

* Principal
* Deputy Principal

---

## access_student_risk_predictions

View student success and risk analytics.

Assigned To:

* Principal
* Guidance and Counselling Teacher

---

# System Permissions

## view_audit_logs

View system activity logs.

Assigned To:

* ICT Administrator
* Principal

---

## manage_system_settings

Modify system settings.

Assigned To:

* ICT Administrator

---

## backup_restore_system

Perform backups and restorations.

Assigned To:

* ICT Administrator

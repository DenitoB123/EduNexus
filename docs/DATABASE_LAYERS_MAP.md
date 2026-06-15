# EduNexus Database Layers Map

## Overview

EduNexus is designed using a modular multi-layer architecture.

Each layer solves a specific school management challenge while remaining connected to the rest of the platform through a centralized user, role, and permission system.

This architecture allows schools to enable only the modules they need while maintaining a single source of truth for all data.

---

# Layer 1 — Core Foundation & Identity Management

## Purpose

Acts as the backbone of the entire platform.

Every module connects to this layer.

## Main Components

- Schools
- Users
- Roles
- Permissions
- User Roles
- Role Permissions

## Solves

- User authentication
- Access control
- Multi-school support
- Role-based permissions
- User identity management

## Connected To

All layers.

---

# Layer 2 — Academic Management System

## Purpose

Manages teaching, learning, curriculum delivery, examinations, and academic records.

## Main Components

- Academic Years
- Terms
- Departments
- Staff
- Students
- Parents
- Classes
- Subjects
- Assignments
- Exams
- Results
- Learning Resources
- Timetables
- Timetable Entries
- Academic Events
- Student Documents

## Solves

- Student enrollment
- Class management
- Teacher assignments
- Curriculum delivery
- Examination management
- Academic record keeping
- Timetable scheduling
- Academic calendar management

## Connected To

- Layer 1 (Users & Roles)
- Layer 3 (Communication)
- Layer 4 (Finance)
- Layer 9 (AI Analytics)

---

# Layer 3 — Communication & Collaboration

## Purpose

Provides communication between all school stakeholders.

## Main Components

- Conversations
- Messages
- Message Reads
- Announcements
- Notifications
- Meetings
- Meeting Participants

## Solves

- Parent communication
- Teacher communication
- Student communication
- School announcements
- Virtual meetings
- Notifications

## Connected To

- Layer 1
- Layer 2
- Layer 9

---

# Layer 4 — Finance Management

## Purpose

Handles all financial operations.

## Main Components

- Fee Categories
- Fee Structures
- Invoices
- Payments
- Receipts
- Scholarships
- Fee Waivers

## Solves

- Fee management
- Billing
- Payment tracking
- Scholarships
- Financial reporting

## Connected To

- Layer 1
- Layer 2
- Layer 9

---

# Layer 5 — Learning Resources Ecosystem

## Purpose

Manages all educational resources available within the school.

## Subsystems

### Library

For reading, borrowing, and returning library books.

### Academic Book Store

For textbook distribution and yearly issuance.

### School Book Shop

Optional module for selling books and learning materials.

### Digital Resource Center

For digital content and learning materials.

## Main Components

- Library Books
- Book Loans
- Book Reservations
- Book Fines
- Academic Book Inventory
- Academic Book Issues
- Academic Book Returns
- Syllabus Completion Tracking
- Book Sales
- Digital Resources

## Solves

- Textbook distribution
- Resource tracking
- Book borrowing
- Book returns
- Digital learning access
- Book sales management

## Connected To

- Layer 2
- Layer 4
- Layer 9

---

# Layer 6 — Boarding & Hostel Management

## Purpose

Supports boarding schools.

Can be disabled for day schools.

## Main Components

- Hostels
- Rooms
- Beds
- Bed Assignments
- Hostel Staff
- Roll Calls
- Leave Requests
- Inspections
- Visitors
- Discipline Records
- Maintenance Requests

## Solves

- Student accommodation
- Roll call management
- Leave tracking
- Hostel discipline
- Visitor management

## Connected To

- Layer 1
- Layer 2
- Layer 3

---

# Layer 7 — Student Life & Co-Curricular Activities

## Purpose

Manages student development outside academics.

## Main Components

- Houses
- Clubs
- Sports Teams
- Leadership Positions
- Events
- Competitions
- Achievements
- Certificates

## Solves

- Student participation tracking
- Leadership management
- Sports management
- Club management
- Talent development

## Connected To

- Layer 2
- Layer 9

---

# Layer 8 — Opportunet

## Purpose

Connects students to opportunities beyond school.

## Main Components

- Opportunity Providers
- Opportunities
- Applications
- Mentors
- Student Profiles
- Recommendation Requests
- Opportunity Matching

## Solves

- Scholarship discovery
- Internship discovery
- Exchange programs
- Career guidance
- University applications
- Mentorship

## Connected To

- Layer 2
- Layer 7
- Layer 9

---

# Layer 9 — AI & Analytics Engine

## Purpose

Provides intelligence across the entire platform.

## Main Components

- Student AI Profiles
- Learning Insights
- Risk Predictions
- Opportunity Recommendations
- Learning Paths
- School Dashboards
- AI Summaries
- Behavior Analytics
- Recommendation Feedback

## Solves

- Performance prediction
- Early risk detection
- Personalized learning
- Opportunity recommendations
- Executive reporting

## Connected To

Every layer.

---

# Layer 10 — Governance, Security & Experience Layer

## Purpose

Controls how users interact with the platform.

## Main Components

### Governance

- Feature Flags
- School Settings

### Security

- IAM Policies
- Sessions
- Audit Logs
- Suspicious Activity Monitoring

### Experience Layer

- UI Layouts
- UI Components
- Personalized Dashboards

### Infrastructure

- API Integrations
- External Synchronization

### Operations

- Inventory Management
- Meal Services
- Transport Management

## Solves

- Access control
- Security monitoring
- Compliance
- Dashboard personalization
- School customization

## Connected To

All layers.

---

# Layer 11 — Workflow Automation & Integration Engine

## Purpose

Automates school processes and reduces manual work.

## Main Components

- Workflows
- Workflow Steps
- Workflow Instances
- Workflow Tasks
- Approvals
- Automations
- Automation Logs
- Webhooks
- Webhook Events

## Solves

- Automated approvals
- Leave request workflows
- Procurement workflows
- Student admission workflows
- Event-triggered actions
- Third-party integrations

## Connected To

All layers.

---

# System Flow

Schools
↓
Users & Roles
↓
Academics
↓
Communication
↓
Finance
↓
Learning Resources
↓
Hostels
↓
Activities
↓
Opportunet
↓
AI Engine
↓
Governance & Security
↓
Workflow Automation

All modules continuously exchange data through the centralized EduNexus platform, creating a unified School Operating System.

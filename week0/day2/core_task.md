# Day 2 – Salesforce Platform Basics

---

## 🔷 CORE TASK 1: Connect Day 1 + Day 2

### How CRM Concepts fit into Salesforce Platform

CRM concepts like Account, Contact, and Opportunity are implemented in Salesforce using Objects and Apps.

- Account → Represents an organization (stored as an Object)
- Contact → Represents a person (stored as an Object)
- Opportunity → Represents a deal (stored as an Object)

### Mapping in Salesforce:
- These are Standard Objects
- They are grouped inside Apps (e.g., Sales App)
- Users access them through Tabs

👉 Example:
Sales App contains:
- Account Tab
- Contact Tab
- Opportunity Tab

This shows how CRM concepts are structured using:
**Objects (data) + Tabs (UI) + Apps (container)**

---

## 🔷 CORE TASK 2: Platform Understanding

### What is an App in Salesforce?
An App is a collection of related components like objects, tabs, dashboards, and workflows designed for a specific business function.

---

### What is an Object?
An Object is a database table that stores data in the form of fields and records.

---

### What is a Tab?
A Tab is a UI element that allows users to access objects and view records.

---

## 🔷 CORE TASK 3: Thinking Task

### When to use Configuration (No Code)?

Use configuration when:
- Requirements are simple
- Standard tools can solve the problem

#### Examples:
1. Creating a validation rule to ensure marks are not negative
2. Creating a workflow to send email alerts automatically

---

### When to use Coding (Apex)?

Use coding when:
- Logic is complex
- Custom functionality is required

#### Examples:
1. Apex Trigger to update multiple related objects automatically
2. Custom Lightning Web Component for dynamic UI behavior

---

## 🔷 CORE TASK 4: Real System Thinking

### System: College Management System

---

### App Name:
College Management App

---

### Objects:

#### Student
- Name
- Roll Number
- Department

#### Faculty
- Name
- Subject

#### Course
- Course Name
- Credits

#### Enrollment
- Student (Lookup)
- Course (Lookup)

---

### User Interaction Flow:

1. User logs into Salesforce
2. Opens "College Management App"
3. Navigates through Tabs (Student, Course, Faculty)
4. Creates and manages records
5. Links students with courses
6. Views reports and dashboards


This makes it powerful and flexible for real-world systems.

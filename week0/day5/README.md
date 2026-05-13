# Apex Introduction

## 1. What is Apex?
Apex is a strongly typed, object-oriented programming language used in Salesforce to write custom business logic. It is used when built-in tools like Flow or Process Builder are not enough to handle complex requirements. Apex runs on Salesforce servers and is similar to Java.

---

## 2. Differences

### Flow vs Apex
Flow is a no-code/low-code tool used for simple automation using a visual interface. Apex is a programming language used for complex logic, integrations, and advanced automation. Flow is easy to maintain, while Apex requires coding knowledge.

### Configuration vs Coding
Configuration means using point-and-click tools without writing code, which is faster and easier for simple tasks. Coding involves writing Apex or components, which is needed for complex business logic and gives more flexibility.

---

## 3. Real Examples Where Apex Is Needed

1. When a student is enrolled in multiple courses, calculate total credits or GPA automatically.
2. When admission status is confirmed, update multiple related records and send notifications.
3. Prevent duplicate student entries based on email or phone number across the system.

---

## 4. Integrated System Design (College Management System)

CRM Mapping:
Account = College
Contact = Student
Lead = Interested Student
Opportunity = Admission Process

Objects:
Student, Faculty, Course, Enrollment

Relationships:
Student → Enrollment (One-to-Many)
Course → Enrollment (One-to-Many)
Enrollment acts as a junction object (Many-to-Many between Student and Course)

Validation:
Marks should not be negative
Email must be unique
Required fields must be filled

Flow:
Send email when admission is confirmed
Auto assign faculty to course

Apex:
Calculate GPA
Handle bulk operations
Apply complex validations across objects

---

## 5. Pseudocode Examples

GPA Calculation:
FOR each student
  GET all courses
  CALCULATE average marks
  UPDATE GPA
END

Prevent Duplicate:
IF email exists
  SHOW error
ELSE
  SAVE
END

Admission Confirmation:
IF status = Confirmed
  SEND email
  UPDATE records
END

---

## 6. Reflection

Enterprise systems need programming because business logic becomes complex, standard tools have limitations, integrations are required, and systems must scale efficiently.

Final Thought:
Salesforce starts with configuration but requires Apex for building powerful real-world applications.

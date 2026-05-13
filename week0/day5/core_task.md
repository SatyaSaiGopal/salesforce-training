# Day 5 – CORE TASKS (College Management System)

---

## 1. Connect Everything Learned Till Now

System: College Management System

CRM:
Student admission pipeline (Lead → Contact → Opportunity → Admission)

Objects:
- Student
- Course
- Faculty
- Enrollment

Relationships:
- Student ↔ Course (Many-to-Many using Enrollment)
- Faculty → Course (One-to-Many)

Validation:
- Email is required for student
- Marks should not be negative

Formula:
- Remaining Seats = Total Seats - Enrolled Students

Flow (Automation):
- Send notification when admission is confirmed
- Auto-assign faculty to courses

Apex (Custom Business Rule):
- Calculate GPA based on multiple courses
- Prevent duplicate student registration
- Apply complex admission eligibility rules

---

## 2. Apex Thinking Exercise

### Case 1: Complex Fee Calculation
Flow is not enough because fee calculation may depend on multiple conditions like scholarships, category, discounts, and installments.
Apex is needed to handle complex conditional logic and calculations.

---

### Case 2: Integration with External Payment System
Flow has limited capability to handle external APIs securely and efficiently.
Apex is required to call external services (payment gateway) and process responses.

---

### Case 3: Advanced Eligibility Logic
Eligibility may depend on multiple subjects, cutoffs, reservation rules, and dynamic conditions.
Flow becomes complicated and hard to maintain.
Apex provides better control and scalability for such logic.

---

## 3. Simple Programming Logic (Pseudocode)

### Case 1: Seat Availability
IF seats are full
  THEN block student registration
END

---

### Case 2: Attendance Rule
IF attendance < 75%
  THEN notify student
END

---

### Case 3: Admission Eligibility
IF marks >= cutoff
  THEN allow admission
ELSE
  reject application
END

---

## 4. Reflection Task

Enterprise systems cannot rely only on clicks and configuration because:

- Business logic becomes very complex
- Configuration tools have limitations
- Advanced conditions are hard to implement visually
- Integration with external systems requires coding
- Performance and scalability need better control

Final Thought:
Configuration is useful for simple and quick solutions, but Apex is necessary for handling real-world, complex enterprise requirements.

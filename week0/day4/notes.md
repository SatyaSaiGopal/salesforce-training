# Day 7 – Salesforce Flow Builder Notes

---

## 🔷 1. Flow Builder Basics

### 🔹 BRIEF NOTES
- Flow Builder = Automation tool in Salesforce
- Used to automate business processes without coding
- Supports different flow types
- Helps reduce manual work

---

### 🔹 DETAILED NOTES

#### What is Flow Builder?
Flow Builder is a point-and-click tool used to automate processes in Salesforce. It allows users to create workflows using a visual interface instead of writing code.

---

#### Why Automation Matters
- Reduces manual effort
- Saves time
- Improves accuracy
- Ensures consistency in business processes

Example:
Instead of manually sending emails, a flow can send them automatically.

---

#### Flow Types

1. Record-Triggered Flow
   - Runs automatically when a record is created/updated

2. Screen Flow
   - Provides UI screens for user interaction

3. Scheduled Flow
   - Runs at a specific time

4. Autolaunched Flow
   - Runs in the background without user interaction

---

#### Business Workflows
Flows are used to automate real-world processes like:
- Admission confirmation
- Email notifications
- Data updates

---

## 🔷 2. Data and Actions in Flows

### 🔹 BRIEF NOTES
- Flows work with records (data)
- Can create, update, delete records
- Uses conditions (decisions)
- Builds logic step by step

---

### 🔹 DETAILED NOTES

#### Working with Records
Flows can:
- Get records (fetch data)
- Create records
- Update records
- Delete records

Example:
Get all students with low attendance

---

#### Updating Data Automatically
Flows can update records without user action.

Example:
When admission is confirmed → update status to "Enrolled"

---

#### Decisions and Conditions
Decision elements are used to apply logic.

Example:
IF marks >= 50
  THEN pass
ELSE
  fail

---

#### Flow Logic
Flow follows a structured path:
Start → Get Data → Decision → Action → End

Example:
1. Record created
2. Check condition
3. Perform action (send email/update record)

---

## 🔷 3. Concepts from Videos

### 🔹 What Flow Builder is
- Visual automation tool
- Drag-and-drop interface
- Easy for beginners

---

### 🔹 Playground Setup
- Used to practice flows
- Safe environment to test automation

---

### 🔹 Basic Automation Understanding
- Trigger → Condition → Action
- Core idea behind all flows

---

### 🔹 Record-Triggered Flow
- Runs when a record is created or updated
- Used for real-time automation

Example:
When student record is created → send welcome email

---

### 🔹 When Flows Execute
- Before save (fast updates)
- After save (more actions possible)

---

### 🔹 Real-World Examples
- Auto-assign faculty to course
- Send admission confirmation emails
- Update student status

---

### 🔹 Why Automation Matters (Business View)
- Improves efficiency
- Reduces human errors
- Speeds up processes

---

### 🔹 Different Automation Types
- Flow Builder
- Process Builder (older)
- Apex (advanced)

---

### 🔹 Visual Overview
Flow Builder uses diagrams:
Start → Elements → Decision → Outcome

---

## 🔷 Duplicate Check Flow

Goal:
Check if student email already exists before saving

Logic:
- Get records with same email
- IF found → show error
- ELSE → allow save

---

## 🔷 FINAL UNDERSTANDING

- Flow Builder = Automation tool (no code)
- Works with data (records)
- Uses decisions (logic)
- Automates business processes

👉 Flow is best for simple automation  
👉 Apex is needed for complex logic

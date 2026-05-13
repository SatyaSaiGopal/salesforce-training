# Apex Learning

---

## 🔷 1. Apex & .NET Basics

### 🔹 BRIEF NOTES
- Apex = Salesforce programming language (like Java)
- Used for writing custom logic
- Supports variables, classes, conditions, loops

---

### 🔹 DETAILED NOTES

#### What is Apex?
Apex is an object-oriented programming language used in Salesforce to execute custom business logic on the platform. It runs on Salesforce servers and is tightly integrated with database operations.

---

#### Variables
Variables are used to store data.

Example types:
- Integer → numbers
- String → text
- Boolean → true/false

Example:
Integer marks = 90
String name = "John"

---

#### Classes
A class is a blueprint that contains variables and methods.

Used to organize code logically.

Example:
Class Student {
  String name;
  Integer marks;
}

---

#### Conditional Logic
Used to make decisions.

IF condition:
IF marks > 50
  THEN pass
ELSE
  fail

---

#### Loops
Used to repeat operations.

Types:
- FOR loop → fixed number of times
- WHILE loop → based on condition

Example:
FOR each student
  print name
END

---

## 🔷 2. Apex Basics & Database

### 🔹 BRIEF NOTES
- Apex syntax similar to Java
- Used to interact with Salesforce database
- Includes DML operations and SOQL queries

---

### 🔹 DETAILED NOTES

#### Apex Syntax
- Case-sensitive
- Uses semicolons
- Follows Java-like structure

---

#### DML Operations (Data Manipulation Language)
Used to modify data in Salesforce.

Types:
- INSERT → add new records
- UPDATE → modify records
- DELETE → remove records

Example:
INSERT student record
UPDATE student marks

---

#### SOQL (Salesforce Object Query Language)
Used to retrieve data from database.

Similar to SQL but designed for Salesforce.

Example:
SELECT Name FROM Student

---

#### Data Manipulation
Combining DML + SOQL to:
- Fetch data
- Process logic
- Update records

---

## 🔷 3. Concepts from Videos

### 🔹 Why Apex Exists
- Flow and configuration cannot handle complex logic
- Apex provides flexibility and control

---

### 🔹 How Apex Works
- Runs on Salesforce servers
- Executes logic before/after database operations
- Works with triggers and classes

---

### 🔹 Hello World Concept
Basic example to display output:
Used to understand syntax and execution

---

### 🔹 Collections
Used to store multiple values:
- List → ordered collection
- Set → unique values
- Map → key-value pairs

---

### 🔹 Logic Building
Breaking problem into steps:
Input → Process → Output

---

### 🔹 Exception Handling
Used to handle errors without crashing program

Example:
TRY
  risky operation
CATCH error
  handle error
END

---

### 🔹 Triggers Overview
Triggers execute automatically when data changes.

Example:
Before insert → validate data
After update → send notification

---

### 🔹 Salesforce CLI Basics
Command-line tool to:
- Deploy code
- Manage projects
- Automate development

---

## 🔷 FINAL UNDERSTANDING

- Apex = Brain of Salesforce logic
- DML = Changes data
- SOQL = Fetches data
- Classes = Structure code
- Loops & Conditions = Build logic
- Triggers = Automate actions

👉 Flow is good for simple tasks  
👉 Apex is required for complex real-world systems

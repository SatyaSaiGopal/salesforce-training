# Day 3: Data Modeling - College Management System

## 1. Core Definitions
* **App:** A container for all the objects, tabs, and features needed for a specific business process (e.g., "College Administration").
* **Object:** A database table (e.g., "Student") that stores specific types of information.
* **Field:** A column in the table (e.g., "Email") that stores a specific piece of data.
* **Record:** An individual row in the table (e.g., a specific student named "John Doe").

---

## 2. Standard vs Custom Objects
* **Standard Objects:** Pre-built by Salesforce (e.g., Accounts, Contacts).
* **Custom Objects:** Built by the admin to meet unique needs (e.g., Students, Courses, Departments).

---

## 3. College Data Model
To manage a college, I have designed the following relationships using **Lookup Relationships**:

| Object | Related To | Relationship Type | Purpose |
| :--- | :--- | :--- | :--- |
| **Student** | **Department** | Many-to-One | Tracks which department a student belongs to. |
| **Course** | **Department** | Many-to-One | Links a specific course to its parent department. |
| **Faculty** | **Department** | Many-to-One | Tracks which department employs the professor. |
| **Course** | **Faculty** | One-to-One | Assigns a specific professor to lead a course. |

---

## 4. Formula Fields (Automated Logic)
I suggest the following 3 formula fields to automate repetitive calculations:

1.  **Student Full Name (Text)**
    * **Logic:** `FirstName & " " & LastName`
    * **Why:** Ensures consistency in reports without manual entry.
2.  **Course Vacancy (Number)**
    * **Logic:** `Total_Seats__c - Enrolled_Students__c`
    * **Why:** Provides real-time visibility into available seats for registration.
3.  **Department Success Rate (Percent)**
    * **Logic:** `Total_Graduates__c / Total_Students__c`
    * **Why:** Helps administration track department performance automatically.

---

## 5. Validation Rules (Data Quality)
I suggest the following 3 rules to block "bad" data:

1.  **Valid Enrollment Age**
    * **Logic:** `Age__c < 16`
    * **Prevents:** Blocks enrollment of students who don't meet the minimum age requirement.
2.  **Institutional Email Only**
    * **Logic:** `NOT(CONTAINS(Email__c, "@college.edu"))`
    * **Prevents:** Ensures students use their official college email addresses.
3.  **Over-Enrollment Guard**
    * **Logic:** `Enrolled_Students__c > Total_Seats__c`
    * **Prevents:** Stops a user from adding students to a course that is already full.

---

## 6. Reflection: Structured Data vs. Spreadsheets
Companies use structured systems like Salesforce instead of Excel because:
1.  **Data Integrity:** Relationships ensure that if a Department name changes, it updates everywhere.
2.  **Scalability:** Databases can handle millions of records without lagging or crashing like a spreadsheet.
3.  **Security:** We can hide sensitive fields (like grades) from unauthorized users, which is hard to do in a shared Excel file.
4.  **Automation:** Formulas and Validation rules work 24/7 to ensure data is correct without human intervention.

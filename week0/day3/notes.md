
# Day 3 Summary: Data Modeling, Formulas, and Validations

## 1. Core Concepts
* **App:** A set of objects, tabs, and other items all working together in one bundle to serve a business process.
* **Object:** Equivalent to a **table** in a database (e.g., Student).
* **Field:** Equivalent to a **column** (e.g., Student Name).
* **Record:** Equivalent to a **row** (e.g., John Doe's specific data).
* **Standard vs. Custom:** Standard objects (Accounts, Contacts) are pre-built by Salesforce; Custom objects are created by us to fit specific needs.

---

## 2. Relationship Types
* **Lookup Relationship:** A "loose" relationship where one object is linked to another. If the parent is deleted, the child remains. (e.g., A Student linked to a Department).
* **Master-Detail:** A "tight" relationship where the child record's existence depends on the parent.
* **Why Relationships Matter:** They prevent data duplication and allow for "Roll-up Summaries" (calculating child data on a parent record).

---

## 3. College Management Data Model (Task 1)
| Object | Relationship | Related To | Logic |
| :--- | :--- | :--- | :--- |
| **Student** | Lookup | **Department** | Many students belong to one department. |
| **Course** | Lookup | **Department** | Departments offer multiple courses. |
| **Faculty** | Lookup | **Department** | Faculty members are assigned to a department. |
| **Course** | Lookup | **Faculty** | One faculty member teaches a specific course. |

---

## 4. Business Logic: Formulas vs. Validations
| Feature | Purpose | Action | Example |
| :--- | :--- | :--- | :--- |
| **Formula Field** | Automation | **Calculates** data automatically. | `EndDate - TODAY()` |
| **Validation Rule** | Prevention | **Blocks** bad data from being saved. | `Age < 18` |

### Task 2: Formula Thinking
1.  **Full Name:** `FirstName & " " & LastName` (Consistently formats names).
2.  **Remaining Seats:** `Total_Seats__c - Enrolled_Students__c` (Real-time availability).
3.  **Course Duration:** `End_Date__c - Start_Date__c` (Automatic length calculation).

### Task 3: Validation Rule Thinking
1.  **Restrict Email:** `NOT(CONTAINS(Email__c, "@college.edu"))` (Ensures official email use).
2.  **Age Check:** `Age__c < 0` (Prevents impossible physical data).
3.  **Seat Limit:** `Enrolled_Students__c > Total_Seats__c` (Prevents classroom overcrowding).

---

## 5. Reflection: Why Structured Data Matters (Task 4)
Companies cannot rely on Excel because:
1.  **Data Integrity:** Structured data ensures that "Department A" is spelled the same way everywhere.
2.  **Security:** You can restrict who sees specific fields (like grades) within an object.
3.  **Automation:** Unlike spreadsheets, Salesforce can automatically trigger emails or calculations when data changes.
4.  **Relationships:** You can instantly see all students related to a course without searching through multiple files.

#Data Modeling, Formulas, and Validations

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

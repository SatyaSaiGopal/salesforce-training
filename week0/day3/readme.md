
# Day 3: Data Modeling, Formulas, and Validation Rules

## 1. Core Salesforce Definitions
* **App:** A collection of tabs and objects that work together to serve a specific business function (e.g., "College Administration").
* **Object:** A database table that stores data about a specific subject (e.g., "Student").
* **Field:** A column within an object that holds a specific piece of information (e.g., "Student Email").
* **Record:** A single row within an object representing an individual item (e.g., a specific student named "Alice Smith").

## 2. Standard vs. Custom Objects
* **Standard Objects:** Included by default with Salesforce (e.g., Accounts, Contacts).
* **Custom Objects:** Created by an administrator to handle unique business needs (e.g., Student, Faculty, Course).

---

## 3. College Data Model
To manage a college effectively, I have designed the following relationships using **Lookup Relationships**:

| Object | Related To | Relationship Type | Purpose |
| :--- | :--- | :--- | :--- |
| **Student** | **Department** | Lookup (1:Many) | Links each student to their specific department. |
| **Faculty** | **Department** | Lookup (1:Many) | Tracks which department a professor belongs to. |
| **Course** | **Department** | Lookup (1:Many) | Connects a course to the department offering it. |
| **Course** | **Faculty** | Lookup (1:1) | Assigns a faculty member as the lead for a course. |

---

## 4. Formula Thinking
Formula fields are essential for **automating calculations** and ensuring data consistency without manual effort.

1.  **Full Name (Text)**
    * **Logic:** `FirstName & " " & LastName`
    * **Why:** It ensures the student's name is always formatted correctly in reports and emails automatically.
2.  **Remaining Seats (Number)**
    * **Logic:** `Total_Seats__c - Enrolled_Students__c`
    * **Why:** Admins need a real-time view of course availability to prevent over-registration.
3.  **Passing Percentage (Percent)**
    * **Logic:** `Marks_Obtained__c / Total_Marks__c`
    * **Why:** It provides instant academic insights without requiring a teacher to calculate grades manually.

---

## 5. Validation Rule Thinking
Validation rules **block invalid data** from entering the system, maintaining high data quality.

1.  **Student Age Verification**
    * **Logic:** `Age__c < 17`
    * **Problem Prevented:** Prevents the enrollment of students who do not meet the minimum age requirement for college.
2.  **Institutional Email Check**
    * **Logic:** `NOT(CONTAINS(Email__c, "@college.edu"))`
    * **Problem Prevented:** Ensures all student records use an official college email address rather than a personal one.
3.  **Seat Limit Guard**
    * **Logic:** `Enrolled_Students__c > Total_Seats__c`
    * **Problem Prevented:** Blocks a registrar from adding a student to a course that is already at full physical capacity.

---

## 6. Reflection & Questions

### Why do companies need structured data instead of spreadsheets?
Structured data in a system like Salesforce allows for **relational integrity**. In a spreadsheet, if you rename a "Department," you have to manually update it in thousands of rows. In Salesforce, you change it once at the source, and every related Student and Course record updates automatically.

---

### 1. Why can’t companies manage everything using Excel sheets?
While Excel is great for simple lists, it fails at the enterprise level because:
* **Lack of Relational Integrity:** Excel is "flat." You cannot easily link a student to a course and a faculty member without duplicating data.
* **Security:** You cannot hide specific columns (like Social Security numbers or Grades) from certain users within the same file easily.
* **Concurrency:** Excel files often get locked when multiple people try to edit them at once, whereas Salesforce allows thousands of simultaneous users.
* **No Audit Trail:** It is difficult to track exactly who changed what value and when in a spreadsheet.

### 2. Why are relationships important between objects?
Relationships (like Lookups and Master-Detail) are the backbone of a database because they:
* **Reduce Data Redundancy:** Instead of typing a Department's address on every Student record, you link the Student to the Department record once.
* **Enable Powerful Reporting:** They allow you to pull data from multiple tables into one view (e.g., "Show me all Students in the CS Department taught by Professor Smith").
* **Maintain Consistency:** Updating the parent record (Department) automatically reflects across all related child records (Students).

### 3. What problems happen if data is inconsistent?
Inconsistent data (e.g., one record says "Dept: Comp Sci" and another says "Dept: CS") leads to:
* **Inaccurate Reporting:** A report on the "Comp Sci" department will miss all the "CS" students.
* **Poor Decision Making:** Leadership might think a department is underperforming simply because the data is fragmented.
* **Loss of Trust:** Users stop relying on the system if they find errors, leading them to go back to using personal spreadsheets.

### 4. Why should repetitive calculations be automated?
Automating calculations through **Formula Fields**:
* **Eliminates Human Error:** A formula never forgets to carry the one or makes a typo.
* **Saves Time:** Users don't have to manually calculate "Days Remaining" or "Total Fees" every time they open a record.
* **Real-Time Accuracy:** Formulas update the instant the underlying data changes, ensuring the information is always current.

### 5. Why should invalid data be blocked early?
Using **Validation Rules** to block bad data at the point of entry is critical because:
* **Clean Data In, Clean Data Out:** It is much cheaper to prevent a mistake than to hire someone to clean up 10,000 bad records later.
* **Process Enforcement:** It ensures business rules are followed (e.g., "No student can be enrolled without an Emergency Contact").
* **System Health:** Invalid data can break downstream automations, such as email alerts or integration with other campus software.

### 6. Why is Salesforce called a metadata-driven platform?
Salesforce is "metadata-driven" because it keeps the **Data** (the actual student names) separate from the **Metadata** (the fields, page layouts, and security rules). 
* When you create a custom field, you are creating metadata. 
* The Salesforce "engine" reads this metadata to render the app on your screen. 
* This allows Salesforce to update their entire platform three times a year without breaking your custom apps, because your customizations are stored as configuration, not hard-coded software.


# Day 2 – Salesforce Platform Basics

## 1. What is Salesforce Platform?

Salesforce Platform is a cloud-based Platform as a Service (PaaS) that allows businesses and developers to build, customize, and deploy applications on top of Salesforce’s infrastructure.

It provides tools for:
- Data storage (Objects)
- User interface (Tabs, Apps)
- Automation (Flows, Process Builder)
- Custom logic (Apex)
- Integration (APIs)

### Key Concept: Multi-Tenant Architecture
Salesforce uses multi-tenant architecture, meaning:
- One shared infrastructure
- Multiple customers (tenants)
- Data is isolated and secure

### Why Salesforce Platform?
- No need to manage servers
- Scalable and secure
- Faster development using configuration + coding
- Built-in CRM features

---

## 2. Explain: App, Object, Tab

### App
An App in Salesforce is a container that groups related functionalities such as objects, tabs, dashboards, and workflows.

👉 Example:
- Sales App
- Service App

Apps help users focus on specific business tasks.

---

### Object
Objects are like database tables used to store data in Salesforce.

Each object contains:
- Fields (columns)
- Records (rows)

#### Types:
- Standard Objects → Account, Contact, Opportunity
- Custom Objects → Created based on business needs

👉 Example:
Student Object:
- Name
- Roll Number
- Course

---

### Tab
Tabs provide a user interface to access objects and records.

Types of Tabs:
- Standard Tab
- Custom Tab
- Visualforce Tab

👉 Example:
A "Student Tab" allows users to view and manage student records.

---

## 3. Difference: Configuration vs Coding

### Configuration (Declarative Approach)
Configuration means building functionality using point-and-click tools without writing code.

#### Used When:
- Logic is simple
- Standard features are sufficient

#### Examples:
1. Creating objects and fields
2. Validation rules to restrict invalid data

---

### Coding (Programmatic Approach)
Coding involves writing code using Apex, Lightning Web Components (LWC), or APIs.

#### Used When:
- Complex business logic is required
- Custom UI or integrations are needed

#### Examples:
1. Apex Trigger to automate complex updates
2. Custom Lightning Component for UI

---

### Key Differences

| Feature        | Configuration            | Coding                |
|----------------|-------------------------|----------------------|
| Approach       | No-code / Low-code      | Full programming     |
| Speed          | Faster                  | Slower               |
| Flexibility    | Limited                 | Highly flexible      |
| Maintenance    | Easy                    | Requires expertise   |

---

## 4. Your System Design (App + Objects + User Interaction)

### System: College Management System

---

### App Name:
College Management App

---

### Objects:

#### 1. Student
- Name
- Roll Number
- Department
- Year

#### 2. Faculty
- Name
- Subject
- Department

#### 3. Course
- Course Name
- Credits

#### 4. Enrollment
- Student (Lookup)
- Course (Lookup)

---

### User Interaction Flow:

1. User logs into Salesforce
2. Selects "College Management App"
3. Navigates using Tabs (Student, Faculty, Course)
4. Creates or views records
5. Links Students to Courses via Enrollment
6. Generates reports (e.g., students per course)

---

### How CRM Fits Into This:
- Student → Similar to Contact
- Faculty → Similar to User/Account
- Course → Custom Object
- Enrollment → Relationship Object

This shows how CRM concepts map to Salesforce Objects. :contentReference[oaicite:0]{index=0}

---

## 5. Screenshots from Trailhead

<img width="1000" height="522" alt="Screenshot 2026-05-11 154421" src="https://github.com/user-attachments/assets/e02c589f-1154-41c0-8b4c-bb2be2d0d52f" />

## **API's and their usage-**
<img width="854" height="783" alt="Screenshot 2026-05-11 154638" src="https://github.com/user-attachments/assets/2a2c3c7c-fd9b-4173-a574-9003a8791b7c" />


---

## Additional Understanding

### When to Use Configuration Instead of Code?
- When requirements are simple
- When standard Salesforce tools can solve the problem

### How Developers Extend Salesforce?
- Using Apex (backend logic)
- Using Lightning Components (UI)
- Using APIs (integration with external systems)

---

## Conclusion

Salesforce Platform provides a powerful mix of:
- Declarative tools (Configuration)
- Programmatic tools (Coding)

This allows both admins and developers to build scalable business applications efficiently.

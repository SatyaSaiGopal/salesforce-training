# Salesforce Platform – Day 2 Notes

These notes summarize all key concepts required to understand how Salesforce works, how CRM fits into it, and how development is done on the platform.

---

## 🔷 1. Salesforce Platform Overview

Salesforce is a cloud-based Platform as a Service (PaaS) that allows users to build applications without managing infrastructure.

### Key Characteristics:
- Runs entirely on the cloud
- No installation required
- Scalable and secure
- Supports both no-code and code-based development

---

## 🔷 2. How Salesforce Works Internally

Salesforce is built on **multi-tenant architecture**.

### Multi-Tenant Architecture:
- One shared platform serves multiple customers
- Each customer’s data is secure and isolated
- Resources are shared efficiently

👉 Simple analogy:
A single apartment building where each tenant has their own private space.

---

## 🔷 3. Core Building Blocks

### 3.1 App
An App is a collection of related components used for a specific business purpose.

Examples:
- Sales App
- Service App

Apps help users focus on their tasks by grouping features.

---

### 3.2 Object
Objects are like database tables that store data.

Each object contains:
- Fields (columns)
- Records (rows)

Types:
- Standard Objects (Account, Contact, Opportunity)
- Custom Objects (created as per requirement)

---

### 3.3 Tab
Tabs are the interface elements that allow users to access objects and their data.

Types:
- Standard Tabs
- Custom Tabs
- Visualforce Tabs

---

## 🔷 4. CRM Concepts in Salesforce

Salesforce is built around CRM (Customer Relationship Management).

### Core CRM Elements:
- Account → Company or organization
- Contact → Individual person
- Opportunity → Sales deal

### How They Fit:
- Stored as **Objects**
- Accessed through **Tabs**
- Organized inside **Apps**

---

## 🔷 5. Development in Salesforce

Salesforce development is done in two ways:

---

### 5.1 Configuration (Declarative Development)

No coding required. Built using point-and-click tools.

#### When to Use:
- Simple logic
- Standard features are enough

#### Examples:
- Creating objects and fields
- Validation rules
- Workflows / Flows

---

### 5.2 Coding (Programmatic Development)

Used for advanced functionality.

#### Tools Used:
- Apex (backend logic)
- Lightning Web Components (UI)
- APIs (integration)

#### When to Use:
- Complex business logic
- Custom UI requirements
- External integrations

---

### Configuration vs Coding

| Aspect        | Configuration        | Coding              |
|---------------|---------------------|--------------------|
| Effort        | Low                 | High               |
| Speed         | Fast                | Slower             |
| Flexibility   | Limited             | High               |

---

## 🔷 6. Admin vs Developer

### Admin (Configuration)
- Uses clicks, not code
- Builds apps quickly

### Developer (Coding)
- Writes Apex and components
- Handles complex logic

---

## 🔷 7. Basic Development Architecture

Salesforce development consists of:

- Data Layer → Objects
- Logic Layer → Apex / Automation
- UI Layer → Tabs, Apps, Components
- Integration Layer → APIs

---

## 🔷 8. Real System Thinking (Example)

### System: College Management

#### App:
College Management App

#### Objects:
- Student
- Faculty
- Course
- Enrollment

#### Flow:
1. User logs in
2. Opens App
3. Uses Tabs to navigate
4. Creates and manages records
5. Views reports

---

## 🔷 9. Trailhead Learning Summary

Modules Covered:
- Platform Basics
- Development Basics

### Key Learnings:
- Structure of Salesforce (Apps, Objects, Tabs)
- Multi-tenant architecture
- Difference between admin and developer roles
- When to use configuration vs coding

---

## 🔷 10. Key Takeaways

- Salesforce = Cloud platform for building applications
- Apps organize features
- Objects store data
- Tabs provide access
- Configuration is for simple tasks
- Coding is for complex logic

---

## ✅ Final Understanding

Salesforce works as a combination of:
- Data (Objects)
- UI (Tabs, Apps)
- Logic (Configuration + Code)

This layered approach makes it powerful, flexible, and easy to scale for real-world business systems.

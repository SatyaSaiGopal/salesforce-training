# Salesforce Platform – Evaluation Questions

---

## 1. What is an App in Salesforce?

An App in Salesforce is a collection of related components such as objects, tabs, dashboards, and workflows that are grouped together to support a specific business function.

Apps provide a focused workspace for users by organizing features in one place.

### Example:
- Sales App → Contains Accounts, Contacts, Opportunities
- Service App → Contains Cases, Knowledge, Reports

---

## 2. What is an Object?

An Object in Salesforce is a database table used to store data.

Each object consists of:
- Fields (columns)
- Records (rows)

### Types of Objects:
- Standard Objects → Predefined (Account, Contact, Opportunity)
- Custom Objects → Created based on business needs

### Example:
Student Object:
- Name
- Roll Number
- Department

---

## 3. Difference between App and Object

| Feature        | App                                      | Object                         |
|----------------|------------------------------------------|--------------------------------|
| Definition     | Collection of components                 | Data storage structure         |
| Purpose        | Organizes UI and features                | Stores data                    |
| Contains       | Tabs, objects, dashboards               | Fields and records             |
| Example        | Sales App                                | Account Object                 |

👉 In simple terms:
- App = Container  
- Object = Data inside the container  

---

## 4. What is Multi-Tenant Architecture? (Basic Understanding)

Multi-tenant architecture means a single shared system (infrastructure and software) serves multiple customers (tenants), while keeping their data separate and secure.

### Key Points:
- Same application instance is shared
- Data is isolated for each user/org
- Resources are efficiently utilized

### Example:
Like an apartment building:
- Building = Salesforce Platform  
- Apartments = Different customers  
- Each apartment is private but shares the same building  

---

## 5. When should we use Configuration instead of Code?

Configuration (no-code) should be used when the requirement can be fulfilled using built-in Salesforce tools without writing code.

### Use Configuration When:
- Logic is simple
- Standard features are sufficient
- Faster implementation is needed

### Examples:
1. Creating validation rules to restrict incorrect data
2. Automating email alerts using Flow or Workflow Rules

---

## 6. How does Salesforce allow developers to extend functionality?

Salesforce allows developers to extend functionality using programmatic tools and integrations.

### Key Methods:

#### 1. Apex (Backend Logic)
- Used to write business logic
- Example: Triggers, Classes

#### 2. Lightning Web Components (Frontend UI)
- Used to build dynamic user interfaces

#### 3. APIs (Integration)
- Connect Salesforce with external systems

#### 4. AppExchange
- Install third-party applications

### Example:
- Creating a custom approval system using Apex
- Integrating payment gateway using APIs

---

## Conclusion

Salesforce provides flexibility through:
- Apps → Organize features  
- Objects → Store data  
- Configuration → Quick solutions  
- Coding → Advanced customization  

This combination helps both admins and developers build scalable applications efficiently.

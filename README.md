College Management - Purchase Request Workflow

Project Overview

This project is developed using the Frappe Framework to implement a complete Purchase Request Management System with Workflow and Role-Based Permissions.

The system allows Employees to create purchase requests, Managers to review and approve them, and Purchase Managers to provide final approval.

---

Technology Stack

- Frappe Framework v15
- Python
- MariaDB
- Git & GitHub
- Ubuntu Linux

---

Purchase Request Doctype

Fields

Field Name| Field Type
Request ID| Data
Item Name| Data
Quantity| Int
Amount| Currency
Reason| Small Text
Workflow State| Data

---

Roles Created

Employee

- Create Purchase Requests
- Review and submit requests

Manager

- Review requests
- Approve or reject requests

Purchase Manager

- Final approval authority
- Complete or reject requests

---

Workflow States

1. Draft
2. Manager Approval
3. Purchase Approval
4. Completed
5. Rejected

---

Workflow Transition Rules

Current State| Action| Next State| Allowed Role
Draft| Review| Manager Approval| Employee
Manager Approval| Approve| Purchase Approval| Manager
Manager Approval| Reject| Rejected| Manager
Purchase Approval| Approve| Completed| Purchase Manager
Purchase Approval| Reject| Rejected| Purchase Manager

---

Complete Workflow Flow

Employee creates Purchase Request

↓

Draft

↓

Review

↓

Manager Approval

↓

Approve

↓

Purchase Approval

↓

Approve

↓

Completed

---

Rejection Flow

Manager Approval

↓

Reject

↓

Rejected

OR

Purchase Approval

↓

Reject

↓

Rejected

---

Permissions Configured

Employee

- Read
- Write
- Create

Manager

- Read
- Write

Purchase Manager

- Read
- Write

---

Testing Performed

Employee Login

Created Purchase Request:

- Request ID
- Item Name
- Quantity
- Amount
- Reason

Clicked Review

Status changed:

Draft → Manager Approval

---

Manager Login

Opened Purchase Request

Clicked Approve

Status changed:

Manager Approval → Purchase Approval

---

Purchase Manager Login

Opened Purchase Request

Clicked Approve

Status changed:

Purchase Approval → Completed

---

Git Commands Used

git add .
git commit -m "Added Purchase Request workflow and doctype"
git push origin develop

---

Repository

GitHub Repository:

https://github.com/Teju2002-alt/college_management

---

Outcome

Successfully implemented a Purchase Request Approval Workflow using Frappe Framework with:

- Custom Purchase Request Doctype
- Role-Based Access Control
- Workflow States
- Workflow Transitions
- User Permissions
- GitHub Version Control

License

MIT

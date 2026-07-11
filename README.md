# ServiceNow Role-Based Project Management System

![ServiceNow](https://img.shields.io/badge/Platform-ServiceNow-81B5A1?style=for-the-badge)
![ACL](https://img.shields.io/badge/Security-Access_Control-blue?style=for-the-badge)
![Flow Designer](https://img.shields.io/badge/Automation-Flow_Designer-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Project-Completed-success?style=for-the-badge)


## 📖 Project Overview

This project demonstrates the implementation of a **Role-Based Project Management System** using the ServiceNow platform.

The application is designed to improve project management by implementing secure role-based access control, automated workflows, and task assignment. Custom roles were created for **Project Managers** and **Team Members**, ensuring that each user can perform only authorized operations.

The solution uses **Access Control Lists (ACLs)** to secure project records and **Flow Designer** to automate project assignment notifications and project completion updates. This implementation demonstrates how ServiceNow can be used to build secure, scalable, and automated business applications.

## ✨ Features

- Custom Project Management Application
- Role-Based Access Control (RBAC)
- Custom Roles
  - Project Manager
  - Team Member
- Record-Level ACLs
- Field-Level ACLs
- Automated Project Assignment Flow
- Automated Project Completion Flow
- Email Notifications
- Custom Number Maintenance (PRO0001...)
- Project Progress Tracking
- Secure Record Visibility

## 🛠 Technologies Used

| Technology           | Purpose                 |
|----------------------|-------------------------|
| ServiceNow           | Application Development |
| ACL                  | Role-Based Security     |
| Flow Designer        | Workflow Automation     |
| Notifications        | Email Automation        |
| Number Maintenance   | Custom Project IDs      |
| Users & Roles        | Access Management       |
| Update Sets          | Application Migration   |


## 🏗 Project Architecture

![Project Architecture](Screenshots/Architecture/Project_Architecture.png)




## 🔄 Project Workflow

The project follows a secure role-based workflow to manage project records efficiently.

1. The **Administrator** creates users and assigns custom roles.
2. The **Project Manager** creates a new project record.
3. The project is assigned to a **Team Member**.
4. An automated **Flow Designer** workflow sends an assignment notification to the assigned user.
5. The Team Member can view only assigned project records because of Record-Level ACLs.
6. The Team Member can update only the **Status** and **Progress Update** fields through Field-Level ACLs.
7. When the project status is changed to **Completed**, a second Flow Designer workflow automatically updates the progress message.
8. The completed project can be reviewed by the Project Manager while maintaining secure access throughout the project lifecycle.

## 🔐 Role-Based Access Control

### Project Manager

- Create Project Records
- Read All Project Records
- Update All Project Records
- Delete Project Records
- Assign Projects to Team Members
- Monitor Project Progress

### Team Member

- View Only Assigned Projects
- Update Project Status
- Update Progress Update Field
- Cannot Create Projects
- Cannot Delete Projects
- Cannot Modify Unauthorized Fields

##  Flow Automation

### Flow 1 – Project Assignment

**Trigger**
- Project record is created.

**Actions**
- Send assignment notification to the assigned Team Member.
- Update the Progress Update field with the initial project status.

---

### Flow 2 – Project Completion

**Trigger**
- Project Status changes to **Completed**.

**Actions**
- Automatically update the Progress Update field with the project completion message.

## 📸 Project Screenshots

## 👤 Users

### Alice User Configuration
![Alice User](Screenshots/01_Users/Alice.png)

### Bob User Configuration
![Bob User](Screenshots/01_Users/Bob.png)

---

## 🔑 Roles

### Project Manager Role
![Project Manager Role](Screenshots/02_Roles/Project_Manager_Role.png)

### Team Member Role
![Team Member Role](Screenshots/02_Roles/Team_Member_Role.png)

---

## 📂 Project Table

### Project Table Configuration
![Project Table](Screenshots/03_Project_Table/1_Project_Table.png)

### Project Form Layout
![Project Form](Screenshots/03_Project_Table/2_Project_Table_Form.png)

### Number Maintenance Configuration
![Number Maintenance](Screenshots/03_Project_Table/3_Number_Maintainance.png)

---

## 🔒 Access Control Lists (ACLs)

### Create ACL
![Create ACL](Screenshots/04_ACLs/1_Create_ACL.png)

### Read ACL
![Read ACL](Screenshots/04_ACLs/2_Read_ACL.png)

### Write ACL
![Write ACL](Screenshots/04_ACLs/3_Write_ACL.png)

### Delete ACL
![Delete ACL](Screenshots/04_ACLs/4_Delete_ACL.png)

### Team Member Read ACL
![Team Member Read ACL](Screenshots/04_ACLs/5_Read_ACL_Team_Member.png)

### State Field ACL
![State Field ACL](Screenshots/04_ACLs/6_Field_ACL_State.png)

### Progress Update Field ACL
![Progress Update Field ACL](Screenshots/04_ACLs/7_Field_ACL_Work_Notes.png)

---

## 📧 Notifications

### Project Assignment Notification
![Project Assignment Notification](Screenshots/05_Notifications/Proejct_Assignment_Notification.png)

### Notification Content
![Notification Content](Screenshots/05_Notifications/What_It_Will_Contain.png)

### Notification Recipients
![Notification Recipients](Screenshots/05_Notifications/Who_Will_Receive.png)

---

## 🔄 Flow Designer

### Project Assignment Flow
![Project Assignment Flow](Screenshots/06_Flow_Designer/1_Project_Assignment_Flow.png)

### Project Completion Flow
![Project Completion Flow](Screenshots/06_Flow_Designer/2_Proejct_Completion_Flow.png)

---

## 🧪 Testing

### Alice - List View
![Alice List View](Screenshots/07_Testing/1_ALice_List_View.png)

### Alice - Form View
![Alice Form View](Screenshots/07_Testing/2_Alice_Form_View.png)

### Bob - List View
![Bob List View](Screenshots/07_Testing/3_Bob_List_View.png)

### Bob - Form View
![Bob Form View](Screenshots/07_Testing/4_Bob_Form_View.png)

---

## ✅ Final Outputs

### Project Assignment Flow Execution
![Project Assignment Flow Output](Screenshots/08_Final_Outputs/1_Project_Assignment_Flow_Output.png)

### Project Assignment Flow Actions
![Project Assignment Flow Actions](Screenshots/08_Final_Outputs/2_Project_Assignment_Flow_Actions.png)

### Project Completion Flow Execution
![Project Completion Flow Output](Screenshots/08_Final_Outputs/3_Project_Completion_Flow_Output.png)

### Completed Project Record
![Completed Project Record](Screenshots/08_Final_Outputs/4_Completed_Project_Record.png)
## Exercise 3: Define roles and users in OpenMRS 

In this exercise, three custom roles were created in OpenMRS to demonstrate role-based access control (RBAC).

### 1. Medical Student
Privileges:
- View Patients
- Get Patients

Inherited Roles:
- Base_PatientViewer

This role allows users to search and view patient information without modifying any data.

---

### 2. Data Assistant
Privileges:
- View Patients
- Get Patients
- Edit Patients

Inherited Roles:
- Base_PatientViewer

This role allows users to search, view, and edit patient information.

---

### 3. Data Manager
Privileges:
- View Patients
- Get Patients
- Edit Patients
- Add Patients

Inherited Roles:
- Data Assistant

This role inherits the privileges of the Data Assistant role and additionally allows users to add new patients into the system.

---

### Created Users

The following users were created and assigned to their corresponding roles:

| Username | Assigned Role |
|----------|---------------|
| yennhi | Medical Student |
| anhquoc | Data Assistant |
| trinhnghi | Data Manager |

---

### RBAC Configuration Evidence

The screenshots demonstrate:
- successful role creation
- role inheritance
- privilege assignment
- successful user-role mapping

---

### Note

Due to the unstable and public nature of the OpenMRS O3 demo server, some frontend navigation menus and patient pages were dynamically restricted despite correct backend RBAC configuration.

However, the RBAC structure, role inheritance, privilege assignment, and user-role mappings were successfully implemented according to the assignment requirements.
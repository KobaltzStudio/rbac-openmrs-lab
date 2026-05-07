<<<<<<< Updated upstream
=======
# Exercise 4: Role Hierarchy Design

In large-scale EHR systems, many roles share common privileges. Instead of assigning all privileges individually to every role, a role hierarchy can be used to reduce duplication and simplify management.

The following base roles were designed:

---

## Base Roles

### Base_PatientEditor

Privileges:

- View Patients
- Add Patients
- Edit Patients

Purpose:
Extends patient viewing capabilities with editing and creation permissions.

---

### Base_EncounterWorker

Privileges:

- Add Encounters
- Edit Encounters
- View Encounters

Purpose:
Handles patient encounter management.

---

### Base_LabWorker

Privileges:

- Add Laboratory Orders
- Edit Laboratory Orders
- View Laboratory Orders

Purpose:
Handles laboratory-related operations.

---

### Base_ReportWorker

Privileges:

- Add Reports
- Edit Reports
- View Reports

Purpose:
Handles report management and generation.

---

### Base_DietWorker

Privileges:

- Add Diet Orders
- Edit Diet Orders
- View Diet Orders

Purpose:
Handles diet order management and generation.

---

### Base_UserManager

Privileges:

- Add Users
- Edit Users
- View Users

Purpose:
Handles user administration tasks.

---

# Final Role Hierarchy

## Nurse

Inherited Roles:

- Base_PatientEditor
- Base_LabWorker
- Base_ReportWorker

Additional Privileges:

- Add/Edit/View Observations

---

## Doctor

Inherited Roles:

- Base_PatientEditor
- Base_LabWorker
- Base_EncounterWorker

Additional Privileges:

- Add/Edit/View Visits

---

## Health Secretary

Inherited Roles:

- Base_EncounterWorker
- Base_DietWorker

---

## Physiotherapist

Inherited Roles:

- Base_EncounterWorker

Additional Privileges:

- Add/Edit/View Physiotherapy Orders

---

## Psychologist

Inherited Roles:

- Base_EncounterWorker
- Base_DietWorker

Additional Privileges:

- Add/Edit/View Psychology Orders

---

## Radiologist

Inherited Roles:

- Base_LabWorker

Additional Privileges:

- Add/Edit/View Radiology Orders

---

## Dentist

Inherited Roles:

- Base_EncounterWorker
- Base_DietWorker

---

## Ambulance Personnel

Additional Privileges:

- View Patients
- Add Reports

---

## System Administrator

Inherited Roles:

- Base_UserManager

Additional Privileges:

- Add/Edit/View Roles
- Add/Edit/View User Passwords

---

## Registration Clerk

Inherited Roles:

- Base_PatientEditor
- Base_UserManager

Additional Privileges:

- Add/Edit/View Appointments

---

# Benefits of the Hierarchy

This hierarchy design:

- reduces privilege duplication
- improves maintainability
- simplifies permission management
- supports scalability
- follows RBAC best practices
>>>>>>> Stashed changes

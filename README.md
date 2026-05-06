# Appendix A — Implemented Role Summary

This appendix summarizes the actual RBAC roles and privileges implemented during the OpenMRS assignment.

---

## Medical Student

Privileges:
- View Patients
- Get Patients

Purpose:
Provides read-only access to patient information.

---

## Data Assistant

Privileges:
- View Patients
- Get Patients
- Edit Patients

Purpose:
Allows viewing and editing of existing patient records.

---

## Data Manager

Privileges:
- View Patients
- Get Patients
- Edit Patients
- Add Patients

Inherited Roles:
- Data Assistant

Purpose:
Extends Data Assistant capabilities by allowing creation of new patient records.

---

# Appendix B — Implemented Role Hierarchy

The following hierarchy was implemented to reduce privilege duplication and improve RBAC maintainability.

```text
Base_PatientViewer
└── Base_PatientEditor
    ├── Doctor
    └── Registration Clerk

Base_LabWorker
├── Nurse
└── Doctor
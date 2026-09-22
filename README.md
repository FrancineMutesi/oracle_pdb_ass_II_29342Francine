# oracle_pdb_ass_II_29342Francine

## INSY 8311 Individual Assignment II - Oracle PDB Management

### Student Information

* **Name:** MUTESI FRANCINE
* **Student ID:** 29342
* **Course:** INSY 8311 - Database Development with PL/SQL
* **Assignment:** Individual Assignment II - Oracle PDB Management

---

## 1. Assignment Overview

This assignment demonstrates the management of Oracle Pluggable Databases (PDBs) in an Oracle Multitenant environment. The practical work includes creating a PDB, creating a user inside the PDB, deleting a temporary PDB, and accessing Oracle Enterprise Manager Database Express.

---

## 2. Oracle Environment

* **Database:** Oracle Database 21c
* **Oracle Version:** 21.3.0.0.0
* **Edition:** Enterprise Edition
* **Operating System:** Microsoft Windows x86 64-bit
* **Database Container:** ORCL
* **SQL Tool:** SQL*Plus

---

## 3. Task 1 - PDB Creation

A new Pluggable Database was created using the required naming format.

### PDB Created

**PDB Name:** `FR_PDB_29342`

### PDB User

**Username:** `FRANCINE_PLSQLAUCA_29342`

The PDB was successfully opened in **READ WRITE** mode, and the user was created inside the PDB.

### Evidence

The Task 1 evidence is stored in:

`screenshots/pdb_creation/`

---

## 4. Task 2 - PDB Deletion

A temporary PDB named:

`FR_TO_DELETE_PDB_29342`

was created for the deletion exercise.

The temporary PDB was then completely removed, including its datafiles.

### Deletion Command

```sql
DROP PLUGGABLE DATABASE FR_TO_DELETE_PDB_29342 INCLUDING DATAFILES;
```

After deletion, the PDB was no longer present in the list of available PDBs.

### Evidence

The Task 2 evidence is stored in:

`screenshots/pdb_deletion/`

Files include:

* `05_temp_pdb_deleted.png`
* `06_temp_pdb_deletion.png`

---

## 5. Task 3 - Oracle Enterprise Manager

Oracle Enterprise Manager Database Express was accessed through the local Oracle environment.

The dashboard displayed the Oracle database environment, including:

* Username: `FRANCINE_PLSQLAUCA_29342`
* Database: `ORCL / FR_PDB_29342`
* Oracle Version: `21.3.0.0.0`
* Database Status: `Up`

### Evidence

The OEM dashboard screenshot is stored in:

`screenshots/oem_dashboard/oem_dashboard.png`

---

## 6. Challenges and Solutions

### Challenge 1 - PDB File Location

During PDB creation, Oracle required a valid `FILE_NAME_CONVERT` configuration.

**Solution:** The source and destination Oracle datafile locations were identified and the PDB was created using the appropriate file conversion path.

### Challenge 2 - Temporary PDB Deletion

The temporary PDB had to be removed completely after verification.

**Solution:** The PDB was dropped using `INCLUDING DATAFILES` so that the associated datafiles were also removed.

### Challenge 3 - Enterprise Manager Access

Initial Enterprise Manager access required the correct PDB context and appropriate Enterprise Manager privileges.

**Solution:** The Enterprise Manager configuration was enabled and the PDB user was granted the required `EM_EXPRESS_BASIC` privilege. The dashboard was then accessed successfully.

---

## 7. Integrity Statement

I confirm that the work and evidence submitted in this repository represent my practical assignment work. I have documented the steps and results associated with my Oracle PDB management tasks and have organized the supporting screenshots in this repository.

---

## 8. Submission Details

| Item                    | Details                                                           |
| ----------------------- | ----------------------------------------------------------------- |
| Repository Link         | https://github.com/FrancineMutesi/oracle_pdb_ass_II_29342Francine |
| PDB Name Created        | `FR_PDB_29342`                                                    |
| Temporary PDB Deleted   | `FR_TO_DELETE_PDB_29342`                                          |
| Issues Encountered      | Yes                                                               |
| OEM Dashboard Completed | Yes                                                               |

---

## 9. Repository Structure

```text
oracle_pdb_ass_II_29342Francine/
│
├── README.md
│
└── screenshots/
    │
    ├── oem_dashboard/
    │   └── oem_dashboard.png
    │
    ├── pdb_creation/
    │   └── ass 2.png
    │
    └── pdb_deletion/
        ├── 05_temp_pdb_deleted.png
        └── 06_temp_pdb_deletion.png
```

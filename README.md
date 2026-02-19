<p align="center">
  <img src="https://www.especial.gr/wp-content/uploads/2019/03/panepisthmio-dut-attikhs.png" alt="UNIWA" width="150"/>
</p>

<p align="center">
  <strong>UNIVERSITY OF WEST ATTICA</strong><br>
  SCHOOL OF ENGINEERING<br>
  DEPARTMENT OF COMPUTER ENGINEERING AND INFORMATICS
</p>

<p align="center">
  <a href="https://www.uniwa.gr" target="_blank">University of West Attica</a> ·
  <a href="https://ice.uniwa.gr" target="_blank">Department of Computer Engineering and Informatics</a>
</p>

---

<p align="center">
  <strong>Databases I</strong>
</p>

<h1 align="center">
  Create and Manage a Database
</h1>

<p align="center">
  <strong>Vasileios Evangelos Athanasiou</strong><br>
  Student ID: 19390005
</p>

<p align="center">
  <a href="https://github.com/Ath21" target="_blank">GitHub</a> ·
  <a href="https://www.linkedin.com/in/vasilis-athanasiou-7036b53a4/" target="_blank">LinkedIn</a>
</p>

<hr>

<p align="center">
  <strong>Supervision</strong>
</p>

<p align="center">
  Supervisor: Periklis Andritsos, Professor
</p>
<p align="center">
  <a href="https://ice.uniwa.gr/en/emd_person/periklis-andritsos/" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/periklisandritsos/" target="_blank">LinkedIn</a>
</p>

<p align="center">
  Co-supervisor: Anastasios Tsolakidis, Assistant Professor<br>
</p>

<p align="center">
  <a href="https://alis.uniwa.gr/en/profile/anastasios-tsolakidis" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/tasos-tsolakidis-35493930/" target="_blank">LinkedIn</a>
</p>

---

<p align="center">
  Athens, May 2023
</p>

---

<p align="center">
  <img src="https://bobcares.com/wp-content/uploads/2022/06/mysql.png" width="250"/>
</p>

---

# README

## Create and Manage a Database

This documentation describes the database schema and SQL operations for managing departments, employees, projects, and assignments.

---

## Table of Contents

| Section | Folder / File                         | Description                             |
| ------: | ------------------------------------- | --------------------------------------- |
|       1 | `assign/`                             | Assignment material                     |
|     1.1 | `assign/assignment_01.pdf`            | Assignment description (English)        |
|     1.2 | `assign/εργασία_01.pdf`               | Assignment description (Greek)          |
|       2 | `docs/`                               | Theoretical and practical documentation |
|     2.1 | `docs/Create-Database.txt`            | Database creation guide (English)       |
|     2.2 | `docs/Δημιουργία-Βάσης-Δεδομένων.txt` | Database creation guide (Greek)         |
|       3 | `Models/`                             | Database schema diagrams                |
|     3.1 | `Models/model_01.png`                 | Schema diagram 1                        |
|     3.2 | `Models/model_02.png`                 | Schema diagram 2                        |
|       4 | `README.md`                           | Project documentation                   |
|       5 | `INSTALL.md`                          | Usage instructions                      |

---

## 1. Database Structure

The database consists of **four interconnected tables**:

### 1.1 Departments (DEPT)

Stores information about company departments.

- **Primary Key:** `DEPTNO`
- **Fields:** `DEPTNO`, `DNAME` (Name), `LOC` (Location)

---

### 1.2 Employees (EMP)

Maintains records for all personnel.

- **Primary Key:** `EMPNO`
- **Foreign Key:** `DEPTNO` (references `DEPT`)
- **Fields:** `EMPNO`, `ENAME`, `JOB`, `HIREDATE`, `MGR` (Manager ID), `SAL` (Salary), `COMM` (Commission), `DEPTNO`

---

### 1.3 Projects (PROJ)

Lists specific projects within the organization.

- **Primary Key:** `PROJ_CODE`
- **Fields:** `PROJ_CODE`, `DESCRIPTION`

---

### 1.4 Assignments (ASSIGN)

Junction table tracking employee project assignments.

- **Primary Key:** Composite Key (`EMPNO`, `PROJ_CODE`)
- **Foreign Keys:**
  - `EMPNO` (references `EMP`)
  - `PROJ_CODE` (references `PROJ`)
- **Fields:** `EMPNO`, `PROJ_CODE`, `A_TIME` (Assigned Time)

---

## 2. Core SQL Operations

### 2.1 Data Definition (DDL)

Commands to create the database and table schemas:

```sql
CREATE DATABASE IF NOT EXISTS new_personnel;

CREATE TABLE DEPT (
    DEPTNO INT PRIMARY KEY,
    DNAME VARCHAR(50),
    LOC VARCHAR(50)
);

CREATE TABLE EMP (
    EMPNO INT PRIMARY KEY,
    ENAME VARCHAR(50),
    JOB VARCHAR(50),
    HIREDATE DATE,
    MGR INT,
    SAL DECIMAL(10,2),
    COMM DECIMAL(10,2),
    DEPTNO INT,
    FOREIGN KEY (DEPTNO) REFERENCES DEPT(DEPTNO)
);

CREATE TABLE PROJ (
    PROJ_CODE INT PRIMARY KEY,
    DESCRIPTION VARCHAR(100)
);

CREATE TABLE ASSIGN (
    EMPNO INT,
    PROJ_CODE INT,
    A_TIME INT,
    PRIMARY KEY (EMPNO, PROJ_CODE),
    FOREIGN KEY (EMPNO) REFERENCES EMP(EMPNO),
    FOREIGN KEY (PROJ_CODE) REFERENCES PROJ(PROJ_CODE)
);
```

---

## 3. Data Manipulation (DML)

### 3.1 Sample data insertion:

```sql
INSERT INTO EMP VALUES (101, 'Codd', 'Analyst', '2020-01-10', NULL, 5000, NULL, 10);
INSERT INTO EMP VALUES (102, 'Elmasri', 'Analyst', '2020-02-15', NULL, 5200, NULL, 10);
INSERT INTO EMP VALUES (103, 'Navathe', 'Salesman', '2020-03-20', NULL, 4800, 200, 20);
INSERT INTO EMP VALUES (104, 'Date', 'Salesman', '2020-04-05', NULL, 4700, 150, 10);
```

---

## 4. Verification

### 4.1 Check the schema and data:

```sql
DESCRIBE DEPT;       -- View table structure
DESCRIBE EMP;
DESCRIBE PROJ;
DESCRIBE ASSIGN;

SELECT * FROM DEPT;   -- View all records
SELECT * FROM EMP;
SELECT * FROM PROJ;
SELECT * FROM ASSIGN;
```

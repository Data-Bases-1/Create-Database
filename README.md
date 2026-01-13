<p align="center">
  <img src="https://www.especial.gr/wp-content/uploads/2019/03/panepisthmio-dut-attikhs.png" alt="UNIWA" width="150"/>
</p>

<p align="center">
  <strong>UNIVERSITY OF WEST ATTICA</strong><br>
  SCHOOL OF ENGINEERING<br>
  DEPARTMENT OF COMPUTER ENGINEERING AND INFORMATICS
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

<p align="center">
  Supervisor: Anastasios Tsolakidis, Assistant Professor<br>
</p>

<p align="center">
  <a href="https://alis.uniwa.gr/en/profile/anastasios-tsolakidis" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/tasos-tsolakidis-35493930/" target="_blank">LinkedIn</a>
</p>

<p align="center">
  Athens, May 2023
</p>

---

# Project Overview

This documentation describes the database schema and SQL operations for managing departments, employees, projects, and assignments.

---

## Table of Contents


| Section | Folder / File | Description |
|------:|---------------|-------------|
| 1 | `assign/` | Assignment material |
| 1.1 | `assign/assignment_01.pdf` | Assignment description (English) |
| 1.2 | `assign/εργασία_01.pdf` | Assignment description (Greek) |
| 2 | `docs/` | Theoretical and practical documentation |
| 2.1 | `docs/Create-Database.txt` | Database creation guide (English) |
| 2.2 | `docs/Δημιουργία-Βάσης-Δεδομένων.txt` | Database creation guide (Greek) |
| 3 | `Models/` | Database schema diagrams |
| 3.1 | `Models/model_01.png` | Schema diagram 1 |
| 3.2 | `Models/model_02.png` | Schema diagram 2 |
| 4 | `README.md` | Repository overview and instructions |

---


## Database Structure

The database consists of **four interconnected tables**:

### 1. Departments (DEPT)
Stores information about company departments.

- **Primary Key:** `DEPTNO`  
- **Fields:** `DEPTNO`, `DNAME` (Name), `LOC` (Location)  

---

### 2. Employees (EMP)
Maintains records for all personnel.

- **Primary Key:** `EMPNO`  
- **Foreign Key:** `DEPTNO` (references `DEPT`)  
- **Fields:** `EMPNO`, `ENAME`, `JOB`, `HIREDATE`, `MGR` (Manager ID), `SAL` (Salary), `COMM` (Commission), `DEPTNO`  

---

### 3. Projects (PROJ)
Lists specific projects within the organization.

- **Primary Key:** `PROJ_CODE`  
- **Fields:** `PROJ_CODE`, `DESCRIPTION`  

---

### 4. Assignments (ASSIGN)
Junction table tracking employee project assignments.

- **Primary Key:** Composite Key (`EMPNO`, `PROJ_CODE`)  
- **Foreign Keys:**  
  - `EMPNO` (references `EMP`)  
  - `PROJ_CODE` (references `PROJ`)  
- **Fields:** `EMPNO`, `PROJ_CODE`, `A_TIME` (Assigned Time)  

---

## Core SQL Operations

### Data Definition (DDL)
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

## Data Manipulation (DML)
### Sample data insertion:

```sql
INSERT INTO EMP VALUES (101, 'Codd', 'Analyst', '2020-01-10', NULL, 5000, NULL, 10);
INSERT INTO EMP VALUES (102, 'Elmasri', 'Analyst', '2020-02-15', NULL, 5200, NULL, 10);
INSERT INTO EMP VALUES (103, 'Navathe', 'Salesman', '2020-03-20', NULL, 4800, 200, 20);
INSERT INTO EMP VALUES (104, 'Date', 'Salesman', '2020-04-05', NULL, 4700, 150, 10);
```

## Verification
### Check the schema and data:
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

## How to Use
1. Initialize Database: Execute `CREATE DATABASE` and `USE new_personnel`;
2. Build Schema: Run `CREATE TABLE` scripts in the order: `DEPT → EMP → PROJ → ASSIGN` to respect foreign key dependencies.
3. Populate Data: Execute `INSERT` commands to load the initial dataset.
4. Verify Data: Use SELECT statements to ensure records are correctly imported. 

---

# Installation & Setup Guide

This repository contains a **relational database creation and management project** developed for the **Databases I (Database Management)** course at the **University of West Attica (UNIWA)**.  
The focus is on creating a sample SQL database, defining tables, inserting sample data, and verifying correct operation.

---

## Prerequisites

To run and explore this project locally, you need:

### 1. Database Management System (DBMS)
- **MySQL** (recommended)
- Any SQL server that supports standard SQL (MariaDB, PostgreSQL with minor adjustments)

Install a local MySQL server or use an online SQL sandbox.

### 2. SQL Client
A tool to execute SQL commands:
- MySQL Workbench
- phpMyAdmin
- DBeaver
- Command‑line MySQL client

Ensure your SQL client is connected to your MySQL server.

---

## Installation

### 1. Clone the Repository

Open a terminal/command prompt and run:

```bash
git clone https://github.com/Data-Bases-1/Create-Database.git
```

#### Alternative (Without Git)

- Open the repository URL in your browser
- Click Code → Download ZIP
- Extract the ZIP file to a local directory

---

## Setting Up the Database
### 2. Open the SQL Files

Navigate into the project:
```bash
Create-Database/
```
Inside, you will find:
- SQL scripts that create the database and tables
- INSERT statements to populate sample data
- SELECT and DESCRIBE commands to validate contents

### 3. Execute SQL Scripts
In your SQL client:
1. Open a new SQL editor session
2. Load the SQL script(s) that define:
   - Creation of the database (CREATE DATABASE)
   - Table definitions (DEPT, EMP, PROJ, ASSIGN)
   - Insertion of sample data
3. Run the full script

#### Example workflow in a MySQL client:
```sql
-- Create the database
CREATE DATABASE new_personnel;

-- Switch to it
USE new_personnel;

-- Create tables and constraints
-- (table definitions here)

-- Insert sample records
-- (INSERT statements here)

-- Verify data
SELECT * FROM DEPT;
SELECT * FROM EMP;
SELECT * FROM PROJ;
SELECT * FROM ASSIGN;
```
If you’re using a SQL file, most clients allow:
```bash
SOURCE path/to/sql-file.sql;
```

---

## Verification

After executing the scripts:

### Verify Tables
```sql
DESCRIBE DEPT;
DESCRIBE EMP;
DESCRIBE PROJ;
DESCRIBE ASSIGN;
```

### Check Sample Records
```sql
SELECT COUNT(*) FROM DEPT;
SELECT COUNT(*) FROM EMP;
SELECT COUNT(*) FROM PROJ;
SELECT COUNT(*) FROM ASSIGN;
```

Correct execution should return no errors, and counts should reflect inserted sample data.

---

## Open the Documentation
1. Navigate to the `docs/` directory
2. Open the report corresponding to your preferred language:
    - English: `Create-Database.txt`
    - Greek: `Δημιουργία-Βάσης-Δεδομένων.txt`
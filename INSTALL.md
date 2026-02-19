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

# INSTALL

## Create and Manage a Database

This repository contains a **relational database creation and management project** developed for the **Databases I (Database Management)** course at the **University of West Attica (UNIWA)**.  
The focus is on creating a sample SQL database, defining tables, inserting sample data, and verifying correct operation.

---

## 1. Prerequisites

To run and explore this project locally, you need:

### 1.1 Database Management System (DBMS)

- **MySQL** (recommended)
- Any SQL server that supports standard SQL (MariaDB, PostgreSQL with minor adjustments)

Install a local MySQL server or use an online SQL sandbox.

### 1.2 SQL Client

A tool to execute SQL commands:

- MySQL Workbench
- phpMyAdmin
- DBeaver
- Command‑line MySQL client

Ensure your SQL client is connected to your MySQL server.

---

## 2. Installation

### 2.1 Clone the Repository

Open a terminal/command prompt and run:

```bash
git clone https://github.com/Data-Bases-1/Create-Database.git
```

### 2.2 Alternative (Without Git)

- Open the repository URL in your browser
- Click Code → Download ZIP
- Extract the ZIP file to a local directory

---

## 3. Setting Up the Database

### 3.1 Open the SQL Files

Navigate into the project:

```bash
Create-Database/
```

Inside, you will find:

- SQL scripts that create the database and tables
- INSERT statements to populate sample data
- SELECT and DESCRIBE commands to validate contents

### 3.2 Execute SQL Scripts

In your SQL client:

1. Open a new SQL editor session
2. Load the SQL script(s) that define:
   - Creation of the database (CREATE DATABASE)
   - Table definitions (DEPT, EMP, PROJ, ASSIGN)
   - Insertion of sample data
3. Run the full script

#### 3.2.1 Example workflow in a MySQL client:

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

## 4. Verification

After executing the scripts:

### 4.1 Verify Tables

```sql
DESCRIBE DEPT;
DESCRIBE EMP;
DESCRIBE PROJ;
DESCRIBE ASSIGN;
```

### 4.2 Check Sample Records

```sql
SELECT COUNT(*) FROM DEPT;
SELECT COUNT(*) FROM EMP;
SELECT COUNT(*) FROM PROJ;
SELECT COUNT(*) FROM ASSIGN;
```

Correct execution should return no errors, and counts should reflect inserted sample data.

---

## 5. Open the Documentation

1. Navigate to the `docs/` directory
2. Open the report corresponding to your preferred language:
   - English: `Create-Database.txt`
   - Greek: `Δημιουργία-Βάσης-Δεδομένων.txt`

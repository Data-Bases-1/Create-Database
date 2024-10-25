![Flag](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Flag_of_the_United_Kingdom_%281-2%29.svg/255px-Flag_of_the_United_Kingdom_%281-2%29.svg.png)

# Database Management and Modeling in MySQL

For the Assignment, click the link:  
[Assignment](Assignment/)

For the Documentation, click the link:  
[Documentation](Documentation/)

For the Model Diagrams, click the link:
[Models](Models/)

---

## Course Information
- **Course**: [Databases I](https://ice.uniwa.gr/education/undergraduate/courses/database-i/)
- **Semester**: 4
- **University**: [University of West Attica](https://www.uniwa.gr/)
- **School**: [School of Engineering](https://www.uniwa.gr/spoydes/scholes-kai-tmimata/feng/)
- **Department**: [Informatics and Computer Engineering](https://ice.uniwa.gr/)
- **Lab Instructor**: [Tsolakidis Anastasios](https://ice.uniwa.gr/emd_person/20879/)
- **Academic Season**: 2022-2023

---

## Student Information
- **Name**: Athanasiou Vasileios Evangelos
- **Student ID**: 19390005
- **Status**: Undergraduate

---

## Assignment Title
**Title**: Creation and Management of a Database and Database Model

---

## Assignment Overview
This assignment involves creating and managing a relational database in SQL for a personnel management system. The project requires:

1. Creating a database named `new_personnel`.
2. Defining and populating four tables: `DEPT`, `EMP`, `PROJ`, and `ASSIGN`.
3. Using SQL commands to:
   - Create the database and tables with appropriate constraints.
   - Insert sample data into each table.
   - Retrieve and verify data from each table.
4. Documenting the structure and data within each table.

---

## Objectives
- Design a database model consisting of four tables:
  - `DEPT`: Stores department details.
  - `EMP`: Stores employee details, including relationships with departments.
  - `PROJ`: Stores project details.
  - `ASSIGN`: Stores employee assignments to projects.
- Ensure referential integrity with foreign keys and primary keys.
- Insert, retrieve, and verify data in each table to demonstrate database functionality.
- Document commands and outputs for database creation and data verification.

---

## Key Features
- **Database Creation**: SQL commands create a database called `new_personnel`.
- **Table Structure**: Each table has defined fields, data types, and primary/foreign keys:
  - `DEPT`: Department details, keyed by `DEPTNO`.
  - `EMP`: Employee details with a foreign key relationship to `DEPT`.
  - `PROJ`: Project details.
  - `ASSIGN`: Assignment of employees to projects, keyed by `EMPNO` and `PROJ_CODE`.
- **Data Insertion**: Sample data is provided for departments, employees, projects, and assignments.
- **Data Retrieval**: Commands retrieve all records to verify data entry.

---

## Program Structure
1. **Database Initialization**  
   - Commands to create `new_personnel` database and switch to it.
   - Commands to define tables and relationships among `DEPT`, `EMP`, `PROJ`, and `ASSIGN`.

2. **Table Definition and Data Insertion**  
   - SQL commands to define each table with field constraints, primary keys, and foreign key relationships.
   - Insertion of sample data into each table, ensuring entries adhere to referential integrity.

3. **Data Verification**  
   - Commands for `DESCRIBE` and `SELECT` statements to verify table structures and inserted data.

---

## Requirements
- **Database System**: MySQL or compatible relational database management system.
- **Software**: Any SQL client for executing commands and querying data.

---

## Installation and Usage
To replicate this project on your local setup, follow these steps:

### 1. Clone the Repository
Download the repository to your local machine:
```
git clone https://github.com/Data-Bases-1/Create-Database.git
```

![Σημαία](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Flag_of_Greece.svg/255px-Flag_of_Greece.svg.png)

# Διαχείριση και Μοντελοποίηση Βάσεων Δεδομένων σε MySQL

Για την Εργασία, κάντε κλικ στον σύνδεσμο:  
[Assignment](Assignment/)

Για την Τεκμηρίωση, κάντε κλικ στον σύνδεσμο:  
[Documentation](Documentation/)

Για τα Μοντέλα Διαγραμμάτων, κάντε κλικ στον σύνδεσμο:
[Models](Models/)

---

## Πληροφορίες Μαθήματος
- **Μάθημα**: [Βάσεις Δεδομένων I](https://ice.uniwa.gr/education/undergraduate/courses/database-i/)
- **Εξάμηνο**: 4ο
- **Πανεπιστήμιο**: [Πανεπιστήμιο Δυτικής Αττικής](https://www.uniwa.gr/)
- **Σχολή**: [Σχολή Μηχανικών](https://www.uniwa.gr/spoydes/scholes-kai-tmimata/feng/)
- **Τμήμα**: [Πληροφορικής και Μηχανικών Υπολογιστών](https://ice.uniwa.gr/)
- **Εργαστηριακός Υπεύθυνος**: [Αναστάσιος Τσολακίδης](https://ice.uniwa.gr/emd_person/20879/)
- **Ακαδημαϊκό Έτος**: 2022-2023

---

## Στοιχεία Φοιτητή
- **Όνομα**: Αθανασίου Βασίλειος Ευάγγελος
- **Αριθμός Μητρώου**: 19390005
- **Κατάσταση**: Προπτυχιακός

---

## Τίτλος Εργασίας
**Τίτλος**: Δημιουργία και Διαχείριση Βάσης Δεδομένων και Μοντέλου Βάσης Δεδομένων

---

## Περιγραφή Εργασίας
Η εργασία περιλαμβάνει τη δημιουργία και διαχείριση μιας σχεσιακής βάσης δεδομένων σε SQL για σύστημα διαχείρισης προσωπικού. Οι απαιτήσεις του έργου είναι οι εξής:

1. Δημιουργία μιας βάσης δεδομένων με όνομα `new_personnel`.
2. Ορισμός και συμπλήρωση τεσσάρων πινάκων: `DEPT`, `EMP`, `PROJ`, και `ASSIGN`.
3. Χρήση εντολών SQL για:
   - Δημιουργία της βάσης και των πινάκων με κατάλληλους περιορισμούς.
   - Εισαγωγή παραδειγματικών δεδομένων σε κάθε πίνακα.
   - Ανάκτηση και επαλήθευση δεδομένων από κάθε πίνακα.
4. Τεκμηρίωση της δομής και των δεδομένων σε κάθε πίνακα.

---

## Στόχοι
- Σχεδίαση ενός μοντέλου βάσης δεδομένων που αποτελείται από τέσσερις πίνακες:
  - `DEPT`: Αποθήκευση στοιχείων τμημάτων.
  - `EMP`: Αποθήκευση στοιχείων εργαζομένων και σχέσεις με τα τμήματα.
  - `PROJ`: Αποθήκευση στοιχείων έργων.
  - `ASSIGN`: Αποθήκευση αναθέσεων εργαζομένων σε έργα.
- Διασφάλιση αναφορικής ακεραιότητας με ξένους και πρωτεύοντες κλειδιά.
- Εισαγωγή, ανάκτηση και επαλήθευση δεδομένων σε κάθε πίνακα για επίδειξη της λειτουργικότητας της βάσης.
- Τεκμηρίωση εντολών και αποτελεσμάτων για τη δημιουργία και επαλήθευση της βάσης δεδομένων.

---

## Κύρια Χαρακτηριστικά
- **Δημιουργία Βάσης Δεδομένων**: Εντολές SQL για δημιουργία της βάσης `new_personnel`.
- **Δομή Πινάκων**: Κάθε πίνακας έχει καθορισμένα πεδία, τύπους δεδομένων και πρωτεύοντα/ξένα κλειδιά:
  - `DEPT`: Λεπτομέρειες τμημάτων, με πρωτεύον κλειδί το `DEPTNO`.
  - `EMP`: Λεπτομέρειες εργαζομένων με ξένο κλειδί που αναφέρεται στον πίνακα `DEPT`.
  - `PROJ`: Λεπτομέρειες έργων.
  - `ASSIGN`: Ανάθεση εργαζομένων σε έργα, με πρωτεύον κλειδί τα `EMPNO` και `PROJ_CODE`.
- **Εισαγωγή Δεδομένων**: Παραδειγματικά δεδομένα παρέχονται για τμήματα, εργαζόμενους, έργα και αναθέσεις.
- **Ανάκτηση Δεδομένων**: Εντολές για την ανάκτηση όλων των εγγραφών για την επαλήθευση των δεδομένων.

---

## Δομή Προγράμματος
1. **Αρχικοποίηση Βάσης Δεδομένων**  
   - Εντολές για δημιουργία της βάσης `new_personnel` και εναλλαγή σε αυτήν.
   - Εντολές για ορισμό πινάκων και σχέσεων μεταξύ των πινάκων `DEPT`, `EMP`, `PROJ`, και `ASSIGN`.

2. **Ορισμός Πινάκων και Εισαγωγή Δεδομένων**  
   - Εντολές SQL για τον ορισμό κάθε πίνακα με περιορισμούς στα πεδία, πρωτεύοντα κλειδιά και ξένα κλειδιά.
   - Εισαγωγή παραδειγματικών δεδομένων σε κάθε πίνακα, διασφαλίζοντας ότι οι εγγραφές πληρούν τους κανόνες αναφορικής ακεραιότητας.

3. **Επαλήθευση Δεδομένων**  
   - Εντολές `DESCRIBE` και `SELECT` για επαλήθευση της δομής των πινάκων και των δεδομένων που έχουν εισαχθεί.

---

## Απαιτήσεις
- **Σύστημα Βάσης Δεδομένων**: MySQL ή συμβατό σύστημα διαχείρισης σχεσιακών βάσεων δεδομένων.
- **Λογισμικό**: Οποιοσδήποτε SQL client για την εκτέλεση εντολών και την αναζήτηση δεδομένων.

---

## Εγκατάσταση και Χρήση
Για να αναπαράγετε αυτό το έργο στον τοπικό σας υπολογιστή, ακολουθήστε τα παρακάτω βήματα:

### 1. Κλωνοποιήστε το Αποθετήριο
Κατεβάστε το αποθετήριο στον τοπικό σας υπολογιστή:
```
git clone https://github.com/Data-Bases-1/Create-Database.git
```
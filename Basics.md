

## 1. Introduction to Databases and SQL

Before working with MySQL, it is important to understand the fundamentals of databases, DBMS, relational databases, and SQL.

### 📌 What is a Database?

A **database** is an organized collection of related data that can be efficiently stored, accessed, managed, and updated.

For example, a college database might contain information about:

* Students
* Courses
* Teachers
* Marks
* Attendance

---

### 🗄️ What is a DBMS?

**DBMS (Database Management System)** is software that allows users and applications to interact with databases.

Instead of directly manipulating the stored data, users interact with the **DBMS**, which manages operations such as:

* Creating data
* Retrieving data
* Updating data
* Deleting data
* Managing database structure
* Controlling access to data

**Basic interaction:**

```text
User / Application
        ↓
       DBMS
        ↓
    Database
```

Examples of DBMS software include:

* MySQL
* Oracle Database
* Microsoft SQL Server
* PostgreSQL

---

### 🔗 What is an RDBMS?

**RDBMS (Relational Database Management System)** is a type of DBMS that stores data in **tables** consisting of rows and columns.

For example:

| ID | Name  | Age |
| -: | ----- | --: |
|  1 | Rahul |  20 |
|  2 | Priya |  21 |
|  3 | Amit  |  19 |

The tables can also be related to each other using concepts such as **primary keys** and **foreign keys**.

Examples of RDBMS:

* MySQL
* Oracle Database
* PostgreSQL
* Microsoft SQL Server

---

### 🌐 What is NoSQL?

**NoSQL (Not Only SQL)** databases generally do not rely on the traditional relational table structure.

They can store data using formats such as:

* Documents
* Key-value pairs
* Graphs
* Wide-column structures

A popular example is **MongoDB**, which primarily uses a document-oriented data model.

> **SQL databases** generally use structured, relational tables, while **NoSQL databases** provide alternative data models that can be more flexible for certain applications.

---

### 💻 What is SQL?

**SQL (Structured Query Language)** is a standard language used to communicate with and manage **relational databases**.

SQL can be used to:

* Create databases and tables
* Insert data
* Retrieve data
* Update data
* Delete data
* Filter and sort data
* Join data from multiple tables
* Aggregate and analyze data

Example:

```sql
SELECT * FROM students;
```

This query retrieves all records from the `students` table.

---

## 🔄 CRUD Operations

CRUD represents the four fundamental operations performed on data.

| Operation      | Meaning       | Purpose                 |
| -------------- | ------------- | ----------------------- |
| **C — Create** | Add data      | Insert new records      |
| **R — Read**   | Retrieve data | View existing records   |
| **U — Update** | Modify data   | Change existing records |
| **D — Delete** | Remove data   | Delete records          |

### Example

```sql
-- Create
INSERT INTO students (name, age)
VALUES ('Rahul', 20);

-- Read
SELECT * FROM students;

-- Update
UPDATE students
SET age = 21
WHERE name = 'Rahul';

-- Delete
DELETE FROM students
WHERE name = 'Rahul';
```

These four operations form the foundation of working with data in database applications.

---

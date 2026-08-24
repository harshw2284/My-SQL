## 2. Database Management

Once the basic database concepts are understood, the next step is learning how to **create, select, view, and delete databases** in MySQL.

A database acts as a **container for tables**, which eventually store the actual data.

---

### 🗂️ Database Management Commands

| Action                 | SQL Syntax              | Example                    |
| ---------------------- | ----------------------- | -------------------------- |
| **Create Database**    | `CREATE DATABASE name;` | `CREATE DATABASE college;` |
| **Delete Database**    | `DROP DATABASE name;`   | `DROP DATABASE temp_db;`   |
| **Select Database**    | `USE name;`             | `USE college;`             |
| **Show All Databases** | `SHOW DATABASES;`       | `SHOW DATABASES;`          |

---

### 1. Create a Database

The `CREATE DATABASE` statement creates a new database.

```sql
CREATE DATABASE college;
```

This creates a database named `college`.

#### Safe Creation

To avoid an error when the database already exists, use `IF NOT EXISTS`:

```sql
CREATE DATABASE IF NOT EXISTS college;
```

This tells MySQL to create the database **only if it does not already exist**.

---

### 2. Show All Databases

The `SHOW DATABASES` command displays all databases available in the current MySQL server.

```sql
SHOW DATABASES;
```

Example output:

```text
+--------------------+
| Database           |
+--------------------+
| college            |
| information_schema |
| mysql              |
| performance_schema |
+--------------------+
```

---

### 3. Select a Database

Before creating or working with tables, you need to tell MySQL which database you want to work with.

Use the `USE` statement:

```sql
USE college;
```

After executing this command, `college` becomes the **currently selected database**.

You can verify the selected database with:

```sql
SELECT DATABASE();
```

---

### 4. Delete a Database

The `DROP DATABASE` command permanently removes a database **along with all of its tables and data**.

```sql
DROP DATABASE temp_db;
```

⚠️ **Be careful:** `DROP DATABASE` is a destructive operation. Once executed, the database and its contents are removed.

#### Safe Deletion

To prevent an error when the database doesn't exist:

```sql
DROP DATABASE IF EXISTS temp_db;
```

---

## 🔄 Typical Database Workflow

A common workflow when starting a MySQL project is:

```sql
-- Create the database
CREATE DATABASE IF NOT EXISTS college;

-- Select the database
USE college;

-- Verify the selected database
SELECT DATABASE();

-- Now create tables...
```

The general structure is:

```text
MySQL Server
│
├── Database 1
│   ├── Table
│   ├── Table
│   └── Table
│
├── Database 2
│   ├── Table
│   └── Table
│
└── Database 3
    └── Table
```

---

## 🧠 Key Takeaways

* `CREATE DATABASE` creates a new database.
* `SHOW DATABASES` displays available databases.
* `USE` selects the database you want to work with.
* `DROP DATABASE` permanently deletes a database and its contents.
* `IF NOT EXISTS` makes database creation safer.
* `IF EXISTS` makes database deletion safer.
* A database should generally be selected with `USE` before creating or accessing its tables.



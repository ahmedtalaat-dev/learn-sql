# Lesson 05: CREATE TABLE 🏗️

## 🎯 Objective
Learn how to create tables in SQL and define columns using appropriate data types.

---

## 📖 What is a Table?

A table is where data is stored in a database.  
It consists of rows and columns.

Each column has:
- A name
- A data type

---

## 🏗️ Creating a Table

To create a table, use the `CREATE TABLE` command:

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype
);
```

✅ Example
```sql
CREATE TABLE users (
    id INT,
    name VARCHAR(50),
    age INT,
    created_at TIMESTAMP
);
```

---

## 🔑 Adding Constraints

Constraints are rules applied to columns.

Common Constraints:
- PRIMARY KEY
- NOT NULL
- UNIQUE
- DEFAULT

✅ Example with Constraints
```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE,
    age INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 🧠 Key Notes
- Choose the correct data type for each column
- Use constraints to ensure data integrity
- Always define a PRIMARY KEY

---

## 🧪 Practice Task
### Create a table called products with:
- id (primary key)
- name (text)
- price (decimal)
- created_at (timestamp)

### Create a table called students with:
- id
- name
- age

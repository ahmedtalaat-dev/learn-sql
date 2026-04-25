# Lesson 07: PRIMARY KEY Constraint 🔑

## 🎯 Objective
Understand the PRIMARY KEY constraint and different ways to define it in SQL.

---

## 📖 What is PRIMARY KEY?

A PRIMARY KEY is a constraint used to uniquely identify each record in a table.

It ensures that:
- Each value is unique  
- No NULL values are allowed  

---

## 🔑 Why Use PRIMARY KEY?

- To uniquely identify each row  
- To prevent duplicate records  
- To improve data integrity  

---

## 🏗️ Method 1: Column-Level Constraint

Define the PRIMARY KEY directly inside the column:

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(100)
);
```

---

## 🏗️ Method 2: Table-Level Constraint

You can give the constraint a custom name:

```sql
CREATE TABLE users (
    id INT,
    first_name VARCHAR(15) NOT NULL,

    CONSTRAINT users_pk PRIMARY KEY (id)
);
```
👉 This helps in managing and modifying constraints later.

---

## ❌ Invalid Example (Duplicate Value)
```sql
INSERT INTO users (id, name)
VALUES (1, 'Ahmed');

INSERT INTO users (id, name)
VALUES (1, 'Ali');
```
👉 Error: PRIMARY KEY must be unique

## ❌ Invalid Example (NULL Value)
```sql
INSERT INTO users (id, name)
VALUES (NULL, 'Ahmed');
```
👉 Error: PRIMARY KEY cannot be NULL

---

## 🧠 Key Notes
- Each table should have one PRIMARY KEY
- It can be defined in multiple ways
- It can be a single column or multiple columns (composite key)
- PRIMARY KEY automatically applies UNIQUE and NOT NULL

---

## 🧪 Practice Task
Create a table called products using:
- PRIMARY KEY inline
- PRIMARY KEY using CONSTRAINT

Try inserting:
- duplicate id
- NULL id

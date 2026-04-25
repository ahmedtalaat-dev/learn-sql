# Lesson 06: Introduction to Constraints 🔒

## 🎯 Objective
Understand what constraints are in SQL and learn how to use the NOT NULL constraint.

---

## 📖 What are Constraints?

Constraints are rules applied to table columns to control the type and validity of data.

They help:
- Ensure data integrity
- Prevent invalid data entry
- Maintain consistency in the database

---

## 🔑 Common Types of Constraints

```sql
NOT NULL
PRIMARY KEY
UNIQUE
DEFAULT
CHECK
FOREIGN KEY
```

---

## 🚫 NOT NULL Constraint
The NOT NULL constraint ensures that a column cannot have a NULL (empty) value.

## 🧠 Why Use NOT NULL?
- To make sure important fields are always filled
- To prevent missing or incomplete data

✅ Example
```sql
CREATE TABLE users (
    id INT,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL
);
```

👉 In this example:

- name cannot be empty
- email cannot be empty

❌ Invalid Example
```sql
INSERT INTO users (id, name, email)
VALUES (1, NULL, 'test@email.com');
```
👉 This will cause an error because name is NOT NULL

---

## 🧠 Key Notes
- NOT NULL is used for required fields
- It improves data quality
- It is commonly used with important columns like name, email

---

## 🧪 Practice Task
Create a table called employees with:
- id
- name (NOT NULL)
- email (NOT NULL)
- Try inserting a row with NULL values and observe the result

# Lesson 09: CHECK Constraint 🧾

## 🎯 Objective
Understand the CHECK constraint and how to use it to enforce rules on column values.

---

## 📖 What is CHECK?

The CHECK constraint is used to limit the values that can be stored in a column by applying a condition.

👉 It ensures that data meets a specific rule before inserting or updating.

---

## 🔑 Why Use CHECK?

- To enforce business rules  
- To validate data automatically  
- To prevent invalid values  

---

## 🏗️ Method 1: Column-Level CHECK

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    age INT CHECK (age >= 18)
);
```

---

## 🏗️ Method 2: Table-Level CHECK
```sql
CREATE TABLE users (
    id INT,
    age INT,
    CONSTRAINT check_age CHECK (age >= 18)
);
```

---

## ❌ Invalid Example
```sql
INSERT INTO users (id, age)
VALUES (1, 15);
```
👉 Error: age must be 18 or older

---

## 🧠 Key Notes
- CHECK defines a condition for valid data
- It works during INSERT and UPDATE
- It helps enforce business logic at database level

---

## 💡 Real World Example
```sql
CREATE TABLE products (
    id INT,
    price DECIMAL(10,2) CHECK (price > 0)
);
```
👉 This ensures product price is always positive

---

## 🧪 Practice Task
Create a table students with:
- id (PRIMARY KEY)
- name
- age (CHECK age >= 18)

Try inserting:
- age = 16 (should fail)
- age = 20 (should succeed)

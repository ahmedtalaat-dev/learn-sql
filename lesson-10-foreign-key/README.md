# Lesson 10: FOREIGN KEY Constraint 🔗

## 🎯 Objective
Understand the FOREIGN KEY constraint and how to create relationships between tables.

---

## 📖 What is FOREIGN KEY?

A FOREIGN KEY is a constraint used to link one table with another.

It ensures that the value in one table must exist in another table.

---

## 🔗 Why Use FOREIGN KEY?

- To create relationships between tables  
- To maintain data consistency  
- To prevent invalid references  

---

## 🧠 Basic Idea

👉 Parent Table (Referenced Table)  
👉 Child Table (Referencing Table)

Example:
- users table → parent  
- orders table → child  

---

## 🏗️ Method 1: Column-Level FOREIGN KEY

```sql
CREATE TABLE orders (
    id INT PRIMARY KEY,
    user_id INT,

    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

---

## 🏗️ Method 2: Table-Level FOREIGN KEY
```sql
CREATE TABLE orders (
    id INT,
    user_id INT,

    CONSTRAINT fk_user
    FOREIGN KEY (user_id)
    REFERENCES users(id)
);
```

---

## 🧠 Key Notes
- FOREIGN KEY must reference a PRIMARY KEY or UNIQUE column
- It enforces referential integrity
- Prevents inserting invalid foreign values

---

## 💡 Real World Example
```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(50)
);

CREATE TABLE orders (
    id INT PRIMARY KEY,
    user_id INT,

    CONSTRAINT fk_orders_user
    FOREIGN KEY (user_id)
    REFERENCES users(id)
);
```

---

## 🧪 Practice Task
Create two tables:
- users (id PRIMARY KEY, name)
- orders (id PRIMARY KEY, user_id FOREIGN KEY)

Try:
- inserting valid user_id
- inserting invalid user_id

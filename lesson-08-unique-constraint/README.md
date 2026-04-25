# Lesson 08: UNIQUE Constraint 🔐

## 🎯 Objective
Understand the UNIQUE constraint and learn the difference between UNIQUE and PRIMARY KEY.

---

## 📖 What is UNIQUE?

The UNIQUE constraint ensures that all values in a column are different.

Unlike PRIMARY KEY, it allows NULL values (depending on the database system).

---

## 🔑 Why Use UNIQUE?

- To prevent duplicate values  
- To enforce data uniqueness  
- Useful for fields like email, phone  

---

## 🏗️ Method 1: Column-Level Constraint

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    email VARCHAR(100) UNIQUE
);
```

---

## 🏗️ Method 2: Table-Level Constraint
```sql
CREATE TABLE users (
    id INT,
    email VARCHAR(100),

    CONSTRAINT unique_email UNIQUE (email)
);
```

---

## ❌ Invalid Example (Duplicate Values)
```sql
INSERT INTO users (id, email)
VALUES (1, 'test@email.com');

INSERT INTO users (id, email)
VALUES (2, 'test@email.com');
```
👉 Error: duplicate value not allowed

---

🧠 Key Notes
- UNIQUE prevents duplicate values
- It can be applied to one or multiple columns
- It can allow NULL values (depending on DBMS)

---

## ⚖️ Difference Between PRIMARY KEY and UNIQUE

| Feature           | PRIMARY KEY 🔑     | UNIQUE 🔐                    |
|------------------|-------------------|------------------------------|
| Uniqueness       | Must be unique    | Must be unique               |
| NULL values      | Not allowed       | Allowed (in most DBMS)       |
| Number per table | Only one          | Multiple allowed             |
| Purpose          | Identify rows     | Prevent duplicates           |

---

## 🧪 Practice Task
Create a table called accounts with:
- id (PRIMARY KEY)
- username (UNIQUE)
- email (UNIQUE)

Try inserting:
- duplicate email
- NULL values

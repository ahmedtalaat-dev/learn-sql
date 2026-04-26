# Lesson 11: Constraints Review 🔁

## 🎯 Objective
Review the most important SQL constraints and understand when to use each one.

---

## 📖 What are Constraints?

Constraints are rules applied to columns to ensure data accuracy and integrity.

---

## 🔑 NOT NULL
Ensures that a column cannot have NULL (empty) values.
```sql
name VARCHAR(50) NOT NULL
```

---

## 🔑 PRIMARY KEY
Uniquely identifies each row in a table.
```sql
id INT PRIMARY KEY
```

---

## 🔑 UNIQUE
Ensures all values in a column are different.
```sql
email VARCHAR(100) UNIQUE
```

---

## 🔑 CHECK
Ensures values meet a specific condition.
```sql
age INT CHECK (age >= 18)
```

---

## 🔑 FOREIGN KEY
Links a column to another table.
```sql
FOREIGN KEY (user_id) REFERENCES users(id)
```

---

## ⚖️ Quick Comparison

| Constraint   | Purpose                       |
|--------------|------------------------------|
| NOT NULL     | Prevent empty values         |
| PRIMARY KEY  | Unique + NOT NULL identifier |
| UNIQUE       | Prevent duplicate values     |
| CHECK        | Enforce condition            |
| FOREIGN KEY  | Link tables                  |

---

## 🧠 Key Notes
- Constraints improve data quality
- Use PRIMARY KEY for identification
- Use FOREIGN KEY for relationships
- Use CHECK for validation rules

---

## 🧪 Practice Task
Create a table employees with:
- id (PRIMARY KEY)
- name (NOT NULL)
- email (UNIQUE)
- age (CHECK age >= 18)

Then:
- Try inserting invalid data and observe errors

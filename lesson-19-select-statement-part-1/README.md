# Lesson 19: SELECT Statement Part 1 🔍

## 🎯 Objective
Learn how to retrieve data from tables using the SELECT statement.

---

## 📖 What is SELECT?

The `SELECT` statement is used to retrieve data from a database.

---

## 🏗️ Basic Syntax

```sql
SELECT column1, column2
FROM table_name;
```

### ✅ Select All Columns
```sql
SELECT * FROM users;
```
👉 * means all columns

### ✅ Select Specific Columns
```sql
SELECT name, age FROM users;
```

### 🏗️ Using Aliases
```sql
SELECT name AS username, age AS user_age
FROM users;
```

### 🏗️ DISTINCT
```sql
SELECT DISTINCT city
FROM customers;
```
👉 Removes duplicate values

---

## 🧠 Key Notes
- SELECT is used to read data
- Use specific columns for better performance
- DISTINCT removes duplicates

---

## 💡 Real Example (Store Project)
```sql
SELECT product_name, list_price
FROM production.products;
```

---

## 🧪 Practice Task
- Select all customers
- Select only names and emails
- Select distinct cities

# Lesson 23: Aggregate Functions 📊

## 🎯 Objective
Learn how to use aggregate functions to perform calculations on data in SQL.

---

## 📖 What are Aggregate Functions?

Aggregate functions perform calculations on multiple rows and return a single value.

---

## 🔑 Common Aggregate Functions

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
```

---

## 🧠 What Each Function Does

| Function | Description                |
|----------|----------------------------|
| COUNT()  | Counts number of rows      |
| SUM()    | Calculates total           |
| AVG()    | Calculates average         |
| MIN()    | Returns smallest value     |
| MAX()    | Returns largest value      |

---

## 🏗️ Examples

🔢 COUNT
```sql
SELECT COUNT(*) FROM sales.customers;
```

➕ SUM
```sql
SELECT SUM(list_price) FROM production.products;
```

📊 AVG
```sql
SELECT AVG(list_price) FROM production.products;
```

🔽 MIN
```sql
SELECT MIN(list_price) FROM production.products;
```

🔼 MAX
```sql
SELECT MAX(list_price) FROM production.products;
```

---

## 💡 Real Example (Store Project)
```sql
SELECT 
    COUNT(*) AS total_products,
    AVG(list_price) AS average_price,
    MAX(list_price) AS highest_price
FROM production.products;
```

---

## 🧠 Key Notes
- Aggregate functions return a single value
- Often used with GROUP BY
- Can be combined in one query

---

## 🧪 Practice Task
- Count number of customers
- Get average product price
- Find highest and lowest price

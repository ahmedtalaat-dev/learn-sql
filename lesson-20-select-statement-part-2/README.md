# Lesson 20: SELECT Statement Part 2 🔎

## 🎯 Objective
Learn how to filter and control query results using WHERE, ORDER BY, and LIMIT.

---

## 🏗️ WHERE Clause

```sql
SELECT * FROM users
WHERE age > 18;
```

## 🏗️ Comparison Operators
```sql
=
!=
>
<
>=
<=
```

## 🏗️ AND / OR
```sql
SELECT * FROM users
WHERE age > 18 AND city = 'Cairo';
```

## 🏗️ LIKE (Pattern Matching)
```sql
SELECT * FROM users
WHERE name LIKE 'A%';
```
👉 Starts with A

## 🏗️ ORDER BY
```sql
SELECT * FROM users
ORDER BY age DESC;
```

## 🏗️ LIMIT (or TOP in SQL Server)
```sql
SELECT TOP 5 * FROM users;
```

---

## 🧠 Key Notes
- WHERE filters data
- ORDER BY sorts results
- LIKE is used for searching
- TOP limits results in SQL Server

---

## 💡 Real Example (Store Project)
```sql
SELECT product_name, list_price
FROM production.products
WHERE list_price > 1000
ORDER BY list_price DESC;
```

---

## 🧪 Practice Task
- Get products with price > 500
- Get customers from a specific city
- Get top 5 products by price

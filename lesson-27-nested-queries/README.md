# Lesson 27: Nested Queries (Subqueries) 🧠

## 🎯 Objective
Understand what subqueries are and how to use them inside SQL statements.

---

## 📖 What is a Subquery?

A subquery (nested query) is a query inside another query.

👉 It is executed first, and its result is used by the main query.

---

## 🧠 Why Use Subqueries?

- To break complex queries into simpler parts  
- To filter data based on another query  
- To perform advanced operations  

---

## 🏗️ Basic Syntax

```sql
SELECT column_name
FROM table_name
WHERE column_name = (
    SELECT column_name
    FROM table_name
    WHERE condition
);
```

---

## ✅ Example 1 (Simple Subquery)
```sql
SELECT product_name, list_price
FROM production.products
WHERE list_price > (
    SELECT AVG(list_price)
    FROM production.products
);
```
👉 Returns products with price above average

---

## 🏗️ Subquery with IN
```sql
SELECT first_name
FROM sales.customers
WHERE customer_id IN (
    SELECT customer_id
    FROM sales.orders
);
```
👉 Returns customers who have orders

---

## 🏗️ Subquery with EXISTS
```sql
SELECT first_name
FROM sales.customers c
WHERE EXISTS (
    SELECT 1
    FROM sales.orders o
    WHERE o.customer_id = c.customer_id
);
```
👉 Returns customers who have at least one order

---

## 💡 Real Example (Store Project)
```sql
SELECT product_name
FROM production.products
WHERE category_id = (
    SELECT category_id
    FROM production.categories
    WHERE category_name = 'Electronics'
);
```

---

## 🧠 Key Notes
- Subqueries are executed first
- Can be used in SELECT, WHERE, FROM
- Powerful but sometimes slower than JOIN

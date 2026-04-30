# Lesson 21: INNER JOIN 🔗

## 🎯 Objective
Understand the concept of JOIN in SQL and learn how to use INNER JOIN to combine data from multiple tables.

---

## 📖 What is JOIN?

JOIN is used to combine rows from two or more tables based on a related column between them.

👉 Usually, this relationship is defined using a FOREIGN KEY.

---

## 🔗 Why Use JOIN?

- To retrieve related data from multiple tables  
- To build meaningful queries  
- To work with relational databases  

---

## 🧠 Basic Idea

Example:
- `customers` table → customer info  
- `orders` table → orders  

👉 We use JOIN to get:
**customer name + order details**

---

## 🏗️ INNER JOIN

INNER JOIN returns only the matching rows between two tables.

---

## 🏗️ Syntax

```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

✅ Example
```sql
SELECT customers.first_name, orders.order_id
FROM sales.customers AS customers
INNER JOIN sales.orders AS orders
ON customers.customer_id = orders.customer_id;
```
👉 This returns:
only customers who have orders

---

## 💡 Real Example (Store Project)
```sql
SELECT p.product_name, c.category_name
FROM production.products AS p
INNER JOIN production.categories AS c
ON p.category_id = c.category_id;
```

---

## 🧠 Key Notes
- INNER JOIN returns matching records only
- Requires a relationship between tables
- Most commonly used JOIN type

---

## 🧪 Practice Task
Join:
- customers with orders
- products with categories

Try:
- selecting specific columns
- using table aliases

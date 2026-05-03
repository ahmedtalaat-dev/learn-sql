# Lesson 28: Views 👁️

## 🎯 Objective
Understand what views are in SQL and how to create and use them.

---

## 📖 What is a View?

A View is a virtual table based on a SQL query.

👉 It does not store data itself  
👉 It shows data from one or more tables

---

## 🧠 Why Use Views?

- Simplify complex queries  
- Improve security (hide columns)  
- Reuse queries easily  

---

## 🏗️ Create a View

```sql
CREATE VIEW view_name AS
SELECT column1, column2
FROM table_name
WHERE condition;
```

---

## ✅ Example
```sql
CREATE VIEW expensive_products AS
SELECT product_name, list_price
FROM production.products
WHERE list_price > 1000;
```
👉 Now you can use it like a table

---

## 🔍 Select from View
```sql
SELECT * FROM expensive_products;
```

## ✏️ Update a View
```sql
ALTER VIEW expensive_products AS
SELECT product_name, list_price
FROM production.products
WHERE list_price > 1500;
```

## ❌ Drop a View
```sql
DROP VIEW expensive_products;
```

---

## 💡 Real Example (Store Project)
```sql
CREATE VIEW customer_orders AS
SELECT 
    c.first_name,
    o.order_id,
    o.order_date
FROM sales.customers c
INNER JOIN sales.orders o
    ON c.customer_id = o.customer_id;
```

---

## 🧠 Key Notes
- Views do not store data
- They always show updated data
- Useful for simplifying JOIN queries

---

## 🧪 Practice Task
Create a view:
- for products with high price
- for customer orders

Try:
- selecting from the view
- modifying the view

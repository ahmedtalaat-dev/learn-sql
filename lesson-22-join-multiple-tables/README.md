# Lesson 22: Join Multiple Tables 🔗🔗

## 🎯 Objective
Learn how to join more than two tables in a single SQL query.

---

## 📖 What Does It Mean?

You can use multiple JOIN statements to combine data from 3 or more tables.

👉 Each JOIN connects two tables using a related column.

---

## 🧠 Basic Idea

Example:
- customers → customer info  
- orders → order info  
- order_items → products in each order  

👉 We join all of them to get:
**customer + order + product details**

---

## 🏗️ Syntax

```sql
SELECT columns
FROM table1
JOIN table2 ON condition
JOIN table3 ON condition;
```

✅ Example (3 Tables)
```sql
SELECT 
    c.first_name,
    o.order_id,
    oi.product_id
FROM sales.customers AS c
INNER JOIN sales.orders AS o
    ON c.customer_id = o.customer_id
INNER JOIN sales.order_items AS oi
    ON o.order_id = oi.order_id;
```
🔍 What This Does
👉 Combines:
- customers
- orders
- order_items

👉 Result:
- each row shows customer + order + product

---

## 💡 Real Example (Store Project)
```sql
SELECT 
    p.product_name,
    b.brand_name,
    c.category_name
FROM production.products AS p
INNER JOIN production.brands AS b
    ON p.brand_id = b.brand_id
INNER JOIN production.categories AS c
    ON p.category_id = c.category_id;
```

---

## 🧠 Key Notes
- You can join unlimited tables
- Always use correct relationships
- Use aliases to keep query clean
- Order of JOIN matters logically

---

## ⚠️ Common Mistakes
- Missing JOIN condition → causes huge incorrect results
- Joining wrong columns
- Forgetting aliases

---

## 🧪 Practice Task
Join:
- customers + orders + stores
- products + brands + categories

Try:
- selecting useful columns
- renaming columns using aliases

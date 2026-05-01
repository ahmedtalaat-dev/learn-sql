# Lesson 24: GROUP BY Clause 📊

## 🎯 Objective
Learn how to group data and apply aggregate functions to each group.

---

## 📖 What is GROUP BY?

The `GROUP BY` clause is used to group rows that have the same values into summary rows.

👉 It is commonly used with aggregate functions like:
- COUNT()
- SUM()
- AVG()

---

## 🧠 Why Use GROUP BY?

- To summarize data  
- To analyze data by category  
- To generate reports  

---

## 🏗️ Basic Syntax

```sql
SELECT column, aggregate_function(column)
FROM table_name
GROUP BY column;
```

---

## ✅ Example
```sql
SELECT category_id, COUNT(*) AS total_products
FROM production.products
GROUP BY category_id;
```
👉 This returns:
number of products in each category

---

## 💡 Real Example (Store Project)
```sql
SELECT brand_id, AVG(list_price) AS average_price
FROM production.products
GROUP BY brand_id;
```

---

## ⚠️ Important Rule
Any column in SELECT must be:
- Either in GROUP BY
- Or inside an aggregate function

---

## ❌ Invalid Example
```sql
SELECT product_name, category_id
FROM production.products
GROUP BY category_id;
```
👉 Error: product_name is not grouped or aggregated

---

## 🧠 Key Notes
- GROUP BY is used with aggregate functions
- It groups rows with same values
- It helps in reporting and analysis

---
## 🧪 Practice Task
- Count products per category
- Get average price per brand
- Group customers by city

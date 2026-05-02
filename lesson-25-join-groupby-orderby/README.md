# Lesson 25: JOIN with GROUP BY & ORDER BY 📊🔗

## 🎯 Objective
Learn how to combine JOIN with GROUP BY and ORDER BY to analyze and organize data effectively.

---

## 📖 What Will You Learn?

- How to JOIN multiple tables  
- How to group results using GROUP BY  
- How to sort results using ORDER BY  

---

## 🧠 Why Combine Them?

👉 In real-world queries, you often need:
- Data from multiple tables (JOIN)  
- Summarized results (GROUP BY)  
- Sorted output (ORDER BY)  

---

## 🏗️ Basic Syntax

```sql
SELECT columns, aggregate_function(column)
FROM table1
JOIN table2 ON condition
GROUP BY column
ORDER BY column;
```

## ✅ Example 1 (Count Orders per Customer)
```sql
SELECT 
    c.first_name,
    COUNT(o.order_id) AS total_orders
FROM sales.customers AS c
INNER JOIN sales.orders AS o
    ON c.customer_id = o.customer_id
GROUP BY c.first_name
ORDER BY total_orders DESC;
```

### 🔍 What This Does
- JOIN customers with orders
- GROUP by customer name
- COUNT number of orders
- ORDER results from highest to lowest

## ✅ Example 2 (Average Product Price per Brand)
```sql
SELECT 
    b.brand_name,
    AVG(p.list_price) AS avg_price
FROM production.products AS p
INNER JOIN production.brands AS b
    ON p.brand_id = b.brand_id
GROUP BY b.brand_name
ORDER BY avg_price DESC;
```
---

## 🧠 Key Notes
- JOIN → combine tables
- GROUP BY → summarize data
- ORDER BY → sort results
- Used together in most real queries

---

## ❌ Common Mistakes
- Forgetting GROUP BY
- Using non-aggregated columns
- Wrong JOIN conditions

---

## 🧪 Practice Task
Get:
- number of orders per store
- average price per category

Try:
- sorting ascending and descending
- grouping by different columns

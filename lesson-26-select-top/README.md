# Lesson 26: SELECT TOP Records 🔝

## 🎯 Objective
Learn how to limit the number of returned rows using TOP in SQL Server.

---

## 📖 What is SELECT TOP?

The `TOP` clause is used to return a specific number of rows from a query.

👉 Useful when:
- You only need part of the data  
- You want top results (highest / lowest)  

---

## 🏗️ Basic Syntax

```sql
SELECT TOP number column_name
FROM table_name;
```

✅ Example
```sql
SELECT TOP 5 *
FROM production.products;
```
👉 Returns first 5 rows

---

## 🏗️ Using TOP with ORDER BY
```sql
SELECT TOP 5 product_name, list_price
FROM production.products
ORDER BY list_price DESC;
```
👉 Returns top 5 most expensive products

---

## 🏗️ TOP with PERCENT
```sql
SELECT TOP 10 PERCENT *
FROM production.products;
```
👉 Returns top 10% of rows

---

## 🏗️ TOP WITH TIES
```sql
SELECT TOP 5 WITH TIES product_name, list_price
FROM production.products
ORDER BY list_price DESC;
```
👉 Includes extra rows if they have the same value as the last row

### 🔍 Example Explanation

If 5th and 6th product have the same price:
👉 Both will be returned

---

## 🧠 Key Notes
- Always use ORDER BY with TOP for meaningful results
- WITH TIES may return more rows than specified
- Useful for ranking-like queries

---

## 🧪 Practice Task
Get:
- top 3 expensive products
- top 5 customers by orders

Try:
- using WITH TIES
- using TOP PERCENT

# Lesson 17: UPDATE Statement ✏️

## 🎯 Objective
Learn how to update existing data in a table using SQL.

---

## 📖 What is UPDATE?

The `UPDATE` statement is used to modify existing records in a table.

---

## 🏗️ Basic Syntax

```sql
UPDATE table_name
SET column1 = value1,
    column2 = value2
WHERE condition;
```

✅ Example
```sql
UPDATE users
SET name = 'Ahmed Ali'
WHERE id = 1;
```
👉 This updates the name of the user with id = 1

---

## ⚠️ Important Warning
If you do not use a WHERE clause:

```sql
UPDATE users
SET name = 'Test';
```
👉 This will update all rows in the table ❗

---

## 🏗️ Update Multiple Columns
```sql
UPDATE users
SET name = 'Ali',
    age = 25
WHERE id = 2;
```

---

## 💡 Real Example (Store Project)
```sql
UPDATE production.products
SET list_price = 999.99
WHERE product_id = 1;
```

---

## ❌ Common Errors
- Forgetting WHERE clause
- Updating wrong column
- Violating constraints

---

## 🧠 Key Notes
- Always use WHERE to control updates
- Double-check conditions before executing
- Constraints still apply during update

---

## 🧪 Practice Task
Update:
- product price
- customer name

Try:
- update multiple rows
- update without WHERE (see what happens carefully)

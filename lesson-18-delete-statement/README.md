# Lesson 18: DELETE Statement 🗑️

## 🎯 Objective
Learn how to delete data from tables using SQL.

---

## 📖 What is DELETE?

The `DELETE` statement is used to remove existing records (rows) from a table.

---

## 🏗️ Basic Syntax

```sql
DELETE FROM table_name
WHERE condition;
```

✅ Example
```sql
DELETE FROM users
WHERE id = 1;
```
👉 This deletes the user with id = 1

---

## ⚠️ Important Warning
If you do not use a WHERE clause:
```sql
DELETE FROM users;
```
👉 This will delete all rows in the table ❗

---

## 🏗️ Delete Multiple Rows
```sql
DELETE FROM users
WHERE age < 18;
```
👉 Deletes all users younger than 18

---

## 🔄 DELETE vs TRUNCATE

| Feature   | DELETE                          | TRUNCATE              |
|----------|----------------------------------|-----------------------|
| Removes  | Specific rows                    | All rows              |
| WHERE    | Supported                        | Not supported         |
| Speed    | Slower                           | Faster                |
| Rollback | Possible (in transaction)        | Not always possible   |

---

## 💡 Real Example (Store Project)
```sql
DELETE FROM production.products
WHERE product_id = 1;
```

---

## ❌ Common Errors
- Forgetting WHERE clause
- Deleting important data
- Violating FOREIGN KEY constraints

---

## 🧠 Key Notes
- Always use WHERE carefully
- Deleting data cannot always be undone
- Constraints may prevent deletion

---

## 🧪 Practice Task
Delete:
- a product
- a customer

Try:
- delete multiple rows
- delete all rows (carefully)

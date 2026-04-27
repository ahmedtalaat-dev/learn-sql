# Lesson 14: ALTER TABLE Part 3 🔄

## 🎯 Objective
Learn how to rename tables and columns in SQL Server.

---

## 📖 Renaming in SQL Server

In SQL Server, renaming is done using the `sp_rename` stored procedure.

---

## ✏️ Rename Table
```sql
EXEC sp_rename 'users', 'customers';
```

## ✏️ Rename Column
```sql
EXEC sp_rename 'users.name', 'full_name', 'COLUMN';
```

---

## 🧠 Key Notes
- sp_rename is specific to SQL Server
- Be careful when renaming tables or columns used in queries
- Renaming may affect existing applications or code

---

## 🧪 Practice Task
- Rename table users to clients
- Rename column name to username

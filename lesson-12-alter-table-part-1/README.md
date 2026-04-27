# Lesson 12: ALTER TABLE Part 1 🛠️

## 🎯 Objective
Learn how to add, modify, and drop columns in a table using ALTER TABLE.

---

## 📖 What is ALTER TABLE?

ALTER TABLE is used to modify an existing table.

---

## ➕ Add Column
```sql
ALTER TABLE users
ADD age INT;
```

## ✏️ Modify Column
```sql
ALTER TABLE users
ALTER COLUMN name VARCHAR(100);
```

## ❌ Drop Column
```sql
ALTER TABLE users
DROP COLUMN age;
```

---

## 🧠 Key Notes
- ALTER TABLE modifies existing tables
- Always be careful when dropping columns
- Changes may affect existing data

---

🧪 Practice Task
- Add a column age to users
- Modify name length
- Drop the age column

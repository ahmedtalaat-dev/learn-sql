# Lesson 16: INSERT INTO ➕

## 🎯 Objective
Learn how to insert data into tables using SQL.

---

## 📖 What is INSERT INTO?

The `INSERT INTO` statement is used to add new records (rows) into a table.

---

## 🏗️ Basic Syntax

```sql
INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3);
```
✅ Example
```sql
INSERT INTO users (id, name, age)
VALUES (1, 'Ahmed', 22);
```

---

## 🏗️ Insert Multiple Rows
```sql
INSERT INTO users (id, name, age)
VALUES 
(3, 'Sara', 21),
(4, 'Mona', 23);
```

---

## ⚠️ Common Errors
- Inserting wrong data type
- Missing required columns (NOT NULL)
- Violating constraints (PRIMARY KEY, UNIQUE, FOREIGN KEY)

---

## 🧠 Key Notes
- Always match columns with values
- Use quotes for text values
- Respect constraints

---

## 💡 Real Example (From Store Project)
```sql
INSERT INTO production.categories (category_name)
VALUES ('Electronics'), ('Clothing');

INSERT INTO production.brands (brand_name)
VALUES ('Nike'), ('Apple');
```

---

## 🧪 Practice Task
Insert data into:
- categories
- brands

Try:
- inserting duplicate PRIMARY KEY
- inserting NULL in NOT NULL column

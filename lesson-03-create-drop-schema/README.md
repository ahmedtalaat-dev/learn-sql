# Lesson 03: Create and Drop Schema 🗂️

## 🎯 Objective
Learn how to create and delete schemas in SQL and understand their role in organizing databases.

---

## 📖 What is a Schema?

A schema is a logical structure that helps organize database objects like tables, views, and procedures inside a database.

Think of it as a "folder inside a database".

---

## 🏗️ Creating a Schema

To create a schema, use the `CREATE SCHEMA` command:

```sql
CREATE SCHEMA schema_name;
```

✅ Example
```sql
CREATE SCHEMA sales;
```

---

## 🗑️ Dropping a Schema

To delete a schema, use the DROP SCHEMA command:
```sql
DROP SCHEMA schema_name;
```
⚠️ Warning
This will permanently delete the schema and all objects inside it.

✅ Example
```sql
DROP SCHEMA sales;
```

---

## 🧠 Key Notes
- Schema helps organize database objects
- One database can contain multiple schemas
- Be careful when dropping a schema

---

## 🧪 Practice Task
- Create a schema called hr
- Create another schema called finance
- Delete the finance schema

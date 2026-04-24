# Lesson 04: Data Types in SQL 📊

## 🎯 Objective
Understand SQL data types and learn the differences between similar types to choose the right one for your data.

---

## 📖 What are Data Types?

Data types define the kind of data that can be stored in a column.
Choosing the correct data type helps:
- Improve performance
- Save storage
- Ensure data accuracy

---

## 🔢 Numeric Data Types

### Common Types
```sql
INT
BIGINT
DECIMAL
FLOAT
```

### 🔍 Differences
#### INT vs BIGINT
- INT → stores normal integer values
- BIGINT → stores very large numbers

👉 Use INT for most cases, and BIGINT when dealing with very large values.

#### DECIMAL vs FLOAT
- DECIMAL → exact precision (used for financial data)
- FLOAT → approximate values (used for scientific calculations)

👉 Example:
```sql
DECIMAL(10,2)
```
10 digits total, 2 after decimal point

---

## 🔤 String Data Types
### Common Types
```sql
CHAR
VARCHAR
TEXT
```

### 🔍 Differences
#### CHAR vs VARCHAR
- CHAR(n) → fixed length (always uses full space)
- VARCHAR(n) → variable length (uses only needed space)

👉 Example:

```sql
CHAR(10) → "Ahmed_____"
```
```sql
VARCHAR(10) → "Ahmed"
```

#### VARCHAR vs TEXT
- VARCHAR → limited length (e.g. 255 characters)
- TEXT → used for large text (descriptions, articles)

---

## 📅 Date and Time Data Types
### Common Types
```sql
DATE
TIME
DATETIME
TIMESTAMP
```

### 🔍 Differences
#### DATE vs DATETIME
- DATE → stores only date (YYYY-MM-DD)
- DATETIME → stores date and time

#### DATETIME vs TIMESTAMP
- DATETIME → fixed value
- TIMESTAMP → auto-updated (useful for tracking changes)

---

## ✅ Boolean Data Type
```sql
BOOLEAN
```
Stores: TRUE or FALSE

---

## 🧠 Key Notes
- Use INT for integers
- Use DECIMAL for money
- Use VARCHAR for most text
- Use TEXT for long content
- Use TIMESTAMP for tracking updates

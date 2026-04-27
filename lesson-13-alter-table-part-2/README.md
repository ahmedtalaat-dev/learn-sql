# Lesson 13: ALTER TABLE Part 2 🔒

## 🎯 Objective
Learn how to add and drop constraints using ALTER TABLE.

---

## ➕ Add Constraint
```sql
alter table store
add constraint 
store_uq unique (store_name)
```

## ❌ Drop Constraint
```sql
alter table store
drop constraint store_uq
```

---

## 🧠 Key Notes
- Some constraints require names to drop
- PRIMARY KEY can only exist once
- Be careful when removing constraints

---

## 🧪 Practice Task
- Add UNIQUE to email
- Add CHECK on age
- Drop one constraint

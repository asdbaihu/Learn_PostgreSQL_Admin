# Liệt kê các foreign key contraints trỏ đến bảng chính

```sql
SELECT *
FROM pg_constraint
WHERE confrelid='film'::regclass
```
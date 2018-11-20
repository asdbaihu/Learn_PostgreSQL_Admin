# Tính tổng số lượng bảng trong 1 database

```sql
SELECT count(*)
FROM information_schema.tables
WHERE table_schema NOT IN ('information_schema', 'pg_catalog')
```
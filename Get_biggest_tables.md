# Lấy 10 bảng lớn nhất trong database

```sql
SELECT table_name, pg_relation_size(table_schema || '.' || table_name) AS size
FROM information_schema.tables
WHERE table_schema NOT IN ('pg_catalog', 'information_schema')
ORDER BY size DESC
LIMIT 10
```
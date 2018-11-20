# Tính xem database tốn bao nhiêu disk space

## Database hiện tại

```sql
SELECT pg_database_size(current_database());
```

## Tổng tất cả các database trong server

```sql
SELECT sum(pg_database_size(datname))
FROM pg_database
```
# Check Postgres server uptime

```sql
SELECT date_trunc('second', current_timestamp - pg_postmaster_start_time()) as uptime;
```

trong đó:

```sql
-- Check Postgres server start time
SELECT pg_postmaster_start_time();
```

```sql
-- Lấy thời gian hiện tại
SELECT current_timestamp;
```
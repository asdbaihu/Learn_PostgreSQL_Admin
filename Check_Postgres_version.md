# Check Postgres Version

## Cách 1: Gửi câu lệnh SQL trên Postgres server

```sql
SELECT version();
```

## Cách 2: Dùng psql

```bash
psql --version
```

## Cách 3: Check file PG_VERSION

```bash
cat $PGDATA/PG_VERSION
```
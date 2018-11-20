# Tính xem 1 bảng tốn bao nhiêu disk space

## Dung lượng bảng = Bảng chính + TOAST table + TOAST index

### Dung lượng bảng chính theo bytes

```sql
SELECT pg_relation_size('actor');
```

### Tổng dung lượng bảng theo bytes

```sql
SELECT pg_total_relation_size('actor');
```

### Lấy dung lượng theo KB/MB/GB

```sql
SELECT pg_size_pretty(pg_total_relation_size('actor'));
```

### TOAST = The Oversize Attribute Storage Technique
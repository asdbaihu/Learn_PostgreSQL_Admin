# psql commands

## Kết nối đến Postgres server

```bash
psql -h 192.168.1.33 -p 2345 -d code123 -U code123
```

- -h: Địa chỉ IP host chứa Postgres server
- -p: Port mà Postgres server expose ra host
- -d: Tên database
- -U: Username

Sau khi chạy câu lệnh trên psql sẽ yêu cầu nhập password

## Thoát khỏi psql

```bash
\q
```

## Có 2 loại command trong psql

- psql meta-command: bắt đầu bằng dấu **"\"**, chạy ở phía psql
- SQL: được gửi đến Postgres server

## Các câu lệnh psql

- Check Postgres version

```sql
psql -U code123 -c "SELECT version()"
````

- Chạy các câu lệnh SQL trong file **.sql**

Tạo file demo.sql có các câu lệnh sau:

```sql
SELECT version();
SELECT current_time;
```

sau đó chạy lệnh:

```bash
psql -U code123 -f demo.sql
```

psql sẽ chạy các lệnh SQL trong file demo.sql
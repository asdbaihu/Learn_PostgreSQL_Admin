# Để kết nối được với PostgreSQL server, cần các tham số:

- Địa chỉ host
- Port
- Tên database
- User
- Password

### Trên 1 host có thể có nhiều Postgres server. Mỗi server expose ra một port khác nhau trên host. Port mặc định của Postgres server là 5432

### Mỗi một Postgres server có thể có 1 hoặc nhiều database

### Host phải explicitly allow connections thì client mới kết nối đến Postgres server được. Hơn nữa, client còn phải cung cấp đúng authentication mà Postgres server qui định

### Client khi connect đến một Postgres server sẽ phải chỉ định rõ tên database muốn kết nối
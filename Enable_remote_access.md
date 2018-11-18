# Kết nối đến Postgres server từ một IP khác

## Cần chỉnh sửa 2 file cấu hình: postgresql.conf và pg_hba.conf

1. Chỉnh sửa file postgresql.conf
Thêm/Chỉnh sửa dòng sau:
```
listen_address = '*'
```
Dòng này có nghĩa chấp nhận kết nối từ mọi địa chỉ IP

2. Chỉnh sửa file pg_hba.conf
Thêm dòng sau vào dòng đầu tiên trong file:
```
# TYPE   DATABASE   USER        CIDR-ADDRESS   METHOD
host        all                   all              0.0.0.0/0              md5
```
Nghĩa là chấp nhận kết nối đến mọi database đối với mọi user có md5 encrypted password hợp lệ

3. Restart Postgres server
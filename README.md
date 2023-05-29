```
# 启动MySQL
docker run --name mysql -e MYSQL_ROOT_PASSWORD=191310630 -p 3306:3306 -d mysql:8
```

```
# 启动Go服务
docker run -d --name scr-sys-server -p 8084:8084 -p 9094:9094 -e DATABASE_TYPE=MYSQL -e "MYSQL_ADDRESS=tcp(124.222.237.67:3306)" -e "MYSQL_USER=root" -e "MYSQL_PASSWORD=191310630" -e "MYSQL_DATABASE=scr-sys" scr-server:v1.0
```

```
# 进入Go服务的内部
docker exec -it #id bash
```

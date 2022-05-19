---
title_: MySQL Memo
trans: MySQL Memo
catagories: Database
date: 2022-5-19
---

# MySQL Memo

## Docker

### Version 5.7

无法通过 host 主机连入数据库.

1. 登录容器

   ```bash
   docker exec -it docker_id bash
   ```

2. 进入 mysql 交互界面

   ```bash
   mysql -u root -p
   ```

3. 创建 `'root'@'%'` 用户

   ```mysql
   CREATE USER 'root'@'%' IDENTIFIED BY 'password';
   ```

4. 赋权

   ```bash
   GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;
   ```

参考: [Host '172.18.0.1' is not allowed to connect to this MySQL server
](https://github.com/docker-library/mysql/issues/275#issuecomment-292208567)

## Common Command

获取数据库数据存储路径

```bash
mysql -uroot -p -e 'SHOW VARIABLES WHERE Variable_Name LIKE "%dir"'
```

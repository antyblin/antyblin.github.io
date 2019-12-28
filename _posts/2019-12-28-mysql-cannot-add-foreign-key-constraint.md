---
layout: post
title:  "MySQL Cannot add foreign key constraint"
---

Подключиться к своей БД и из-под рута выполнить команду:
```sql
show engine innodb status;
```

Среди прочего можно увидеть подробную информацию по последней ошибке добавления ограничения FK.

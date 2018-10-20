---
title: SQL Create Table Statement
localeTitle: SQL Создание таблицы
---
## SQL Создание таблицы

Таблица представляет собой группу данных, хранящихся в базе данных.

Чтобы создать таблицу в базе данных, вы используете оператор `CREATE TABLE` . Вы указываете имя таблицы и список столбцов с их типами данных.
```
CREATE TABLE TABLENAME(Attribute1 Datatype, Attribute2 Datatype,........); 
```

Вот пример создания таблицы с именем Person:

```sql
CREATE TABLE Person( 
  Id int not null, 
  Name varchar not null, 
  DateOfBirth date not null, 
  Gender bit not null, 
  PRIMARY KEY( Id ) 
 ); 
```

В приведенном выше примере каждое лицо имеет имя, дату рождения и пол. Столбец Идентификатор - это ключ, который идентифицирует одного человека в таблице. Вы используете ключевое слово `PRIMARY KEY` для настройки одного или нескольких столбцов в качестве первичного ключа.

Столбец может быть `not null` или `null` указывающим, является ли он обязательным или нет.

#### Дополнительная информация:
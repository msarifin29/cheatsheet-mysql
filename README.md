# cheatsheet-mysql

| description | code |
| ---  | ---  | 
| connect to mysql | `mysql -u{name user} -p` |
| create new database  | `create database {name database};` |
| delete database | `drop database {name database};` |
| use database | `use {name database};` |
| create table | `create table {name table};` |
| show description table | `desc {name table};` |
| show table | `show create table {name table};` |
| add column | `alter table {name table} add column {name column} {type};` |
| add column with value not null | `alter table {name table} add column {name column} {type} not null;` |
| add column with value not null and default value timestamp | `alter table {name table} add column {name column} timestamp not null default current_timestamp;` |
| rename column | `alter table {name table} rename column {old name column} to new name column};` |
| edit column | `alter table {name table} modify {name column} {new type};` |


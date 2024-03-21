### Database and Table
| description | code |
| ---  | ---  | 
| connect to mysql | `mysql -u{name user} -p` |
| create new  | `create database {name database};` |
| delete | `drop database {name database};` |
| use database | `use {name database};` |
| create table | `create table {name table};` |
| rename table | `rename table {old table} {new table};` |
| show description table | `desc {name table};` |
| show table | `show create table {name table};` |
### Column
| description | code |
| ---  | ---  | 
| add column | `alter table {name table} add column {name column} {type column};` |
| default value not null | `alter table {name table} add column {name column} {type} not null;` |
| default value | `alter table {name table} add column {name column} timestamp not null default current_timestamp;` |
| rename column | `alter table {name table} rename column {old name column} to {new name column};`flag `after {x column}`to shift after x column.  |
| edit column | `alter table {name table} modify {name column} {new type};` |
| delete column | `alter table {name table} drop column {name column};` |
| delete table and create new table | `truncate {name table};` |
| delete permanent | `drop table {name table};` |
| insert data | `insert into {name table}({name column}) values({input value});` |
| delete foreign key | `alter table {name table} drop constraint {name foreign key};` |
| add unique key | `alter table {name table} add constraint {name unique key} unique({name column});` |
| delete unique key | `alter table account drop constraint email_unique;` |
| add or delete check constraint | `alter table {name table} add constraint {name constraint} check {condition};` |
| add index | `alter table {name table} add index {name index} ({name column});` |
| delete index | `alter table {name table} drop index {name index};` |
### Select
| description | code |
| ---  | ---  |
| all | `select * {name table};` |
| get specifice data by column | `select {name column} from {name table};` |
| add primary key | `alter table {name table} add primary key ({name column});` |
| filter | `select * from {name table} where {condition};` |
| delete all | `delete from {name table` |
| update 1 column | `update {name table} set {name column} = {new value} where {conditoion};` |
| update many column | `update {name table} set {name column} = {value} where {name column A} in ({data column A});` |
| delete 1 column | `delete from {name table} where {condition};` |
| by order with maximal | `select * from {name table} where {name column} {condition} order by {name column} limit {number};` |
| alias | `select {name column} as {name alias} from {name column}` |
| like operator | | `LIKE 'b%'` value with first keyword b `LIKE '%a'` value with end keyword a `LIKE %abc%` value constaint of abc `NOT LIKE` not like|
| null | `select * from {name table} where {name column} is null` or `not null` if not null |
| order by clause | `select * from {name table} order by {name column} ASC, {name column} DESC` from small to bigger `ASC` bigger to small `DESC` |
| limit clause | `select * from {name table} order by {name column} limit {number of limit}` |
| offset or skip or pagination | `select * from {name table} order by {name column} limit 5, 5`  |
| reomve duplicate value | `select distinct {name column} from {name table}` |
| arithmetic operator | `select id, name, price DIV 1000 as 'price in K' from product` division price or '/'  |
| else if condition | `select {name column} if({conditon}, {value}, {another value}) from {name table};` |
| switch case | `select {name column} case {name column} when {name value} then {return value} else {return value} end as {name alias} from {name table};` |
| if condition with nullable | `select {name colum} ifnull({name column, {return value}) from {name table};` |
| grouping with maximal value | `select max({name column}) as {name alias} from product group by {name column};` |
| filter grouping | `select count({name column}) as {name alias} from {name table} group by {name column} having {condition};` |
| add Full-Text Search | `alter table {name table} add fulltext {name full text search} ({name column});` |
| delete Full-Text Search | `alter table {name table} index {name full text search};` |
| find by natural language | `select * from {name table} where match({name column}) against("keyword" in natural language mode);` |
| find by query expansion | `select * from {name table} where match({name column}) against("keyword" with query expansion);` |
| add relation table with foreign key | `alter table {name table} add constraint {name foreign key} foreign key ({column forein key}) references {name table} ({name column});` |
### Join
| description | code |
| ---  | ---  |
| join table with specifice table | `select whishlist.id_product, products.id, whishlist.description, products.name from whishlist join products on (whishlist.id_product =  products.id);` |
| join one to one table | `select {name column A}, {name column B} from {name table B} join {name table A} on ({foreign key A} = {foreign key B});` |
| relation from table A dan table B | `select * from {name table A} inner join {name table B} on ({name column foreign key A} = {name column foreign key B});` |
| relation of left table | `select * from {name table A} left join {name table B} on ({name column foreign key A} = {name column foreign key B});` |
| relation of right table | `select * from {name table A} right join {name table B} on ({name column foreign key A} = {name column foreign key B});` |
| join many to many | `select {name column A}, {name column B}, {name column B}, {name column C} from {name table C} join {name table B} on ({foreign key B} = {foreign key C}) join {name table A} on ({foreign key A} = {foreign key C});` |
| backup database | `mysqldump {name database} --user root --password --result-file={location file}{name database}.sql` |
| restore database | `source {location file mysql};` |
| 




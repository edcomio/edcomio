+--------------------+
| Database           |
+--------------------+
| information_schema |
| movies             |
| mysql              |
| performance_schema |
| seriesdb_schema    |
| sys                |
+--------------------+
6 rows in set (0.0016 sec)
 MySQL  localhost:3306 ssl  movies  SQL > use seriesdb_schema;
Default schema set to `seriesdb_schema`.
Fetching table and column names from `seriesdb_schema` for auto-completion... Press ^C to stop.
 MySQL  localhost:3306 ssl  seriesdb_schema  SQL > create table director(id int not null auto_increment,name varchar(256)not null,primmary key(id))
                                                -> ;
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'key(id))' at line 1
 MySQL  localhost:3306 ssl  seriesdb_schema  SQL > create table director(id int not null auto_increment,name varchar(256)not null,primmary key(id));
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'key(id))' at line 1
 MySQL  localhost:3306 ssl  seriesdb_schema  SQL > create table director(id int not null auto_increment,name varchar(256)not null,primary KEY(id));
Query OK, 0 rows affected (0.0731 sec)
 MySQL  localhost:3306 ssl  seriesdb_schema  SQL > show tables;
+---------------------------+
| Tables_in_seriesdb_schema |
+---------------------------+
| director                  |
+---------------------------+
1 row in set (0.0018 sec)
 MySQL  localhost:3306 ssl  seriesdb_schema  SQL > create database series;
Query OK, 1 row affected (0.0095 sec)
 MySQL  localhost:3306 ssl  seriesdb_schema  SQL > use series;
Default schema set to `series`.
Fetching table and column names from `series` for auto-completion... Press ^C to stop.
 MySQL  localhost:3306 ssl  series  SQL > create table director(id int not null auto_increment,name varchar(256)not null,primary KEY(id));
Query OK, 0 rows affected (0.0480 sec)
 MySQL  localhost:3306 ssl  series  SQL > show tables;
+------------------+
| Tables_in_series |
+------------------+
| director         |
+------------------+
1 row in set (0.0040 sec)
 MySQL  localhost:3306 ssl  series  SQL > describe director;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0135 sec)
 MySQL  localhost:3306 ssl  series  SQL > create database seriesdb;
Query OK, 1 row affected (0.0103 sec)
 MySQL  localhost:3306 ssl  series  SQL > use seriesdb;
Default schema set to `seriesdb`.
Fetching table and column names from `seriesdb` for auto-completion... Press ^C to stop.
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table director(id int not null auto_increment,name varchar(256)not null,primary KEY(id));
Query OK, 0 rows affected (0.0360 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table country(id int not null auto_increment,name varchar(256)not null,primary KEY(id));
Query OK, 0 rows affected (0.0342 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe country;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0150 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe series;
ERROR: 1146 (42S02): Table 'seriesdb.series' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe seriesdb;
ERROR: 1146 (42S02): Table 'seriesdb.seriesdb' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int not null auto_increment,name varchar(256)not null,genre int not null ,director int not null,country int not null,yor int not null,yoe int not null, primary KEY(id));
Query OK, 0 rows affected (0.0361 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe series;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int          | NO   | PRI | NULL    | auto_increment |
| name     | varchar(256) | NO   |     | NULL    |                |
| genre    | int          | NO   |     | NULL    |                |
| director | int          | NO   |     | NULL    |                |
| country  | int          | NO   |     | NULL    |                |
| yor      | int          | NO   |     | NULL    |                |
| yoe      | int          | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
7 rows in set (0.0142 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int not null auto_increment,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256)not null,yor int not null,yoe int not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int not null auto_increment,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256)not null,yor int not null,yoe int not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe series;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int          | NO   | PRI | NULL    | auto_increment |
| name     | varchar(256) | NO   |     | NULL    |                |
| genre    | int          | NO   |     | NULL    |                |
| director | int          | NO   |     | NULL    |                |
| country  | int          | NO   |     | NULL    |                |
| yor      | int          | NO   |     | NULL    |                |
| yoe      | int          | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
7 rows in set (0.0018 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int not null auto_increment,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256) not null,yor int not null,yoe int not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe series;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int          | NO   | PRI | NULL    | auto_increment |
| name     | varchar(256) | NO   |     | NULL    |                |
| genre    | int          | NO   |     | NULL    |                |
| director | int          | NO   |     | NULL    |                |
| country  | int          | NO   |     | NULL    |                |
| yor      | int          | NO   |     | NULL    |                |
| yoe      | int          | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
7 rows in set (0.0019 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int not null auto_increment,name varchar(256)not null,genre int not null ,director int not null,country int not null,status int  not null,yor int not null,yoe int not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int not null auto_increment,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256) not null,yor int not null,yoe int not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(status varchar(256) not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table Status( varchar(256) not null, primary KEY(id));
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'varchar(256) not null, primary KEY(id))' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
Empty set (0.0009 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series(name,genre,director,country,yor,yoe)values
                                         ->
                                         ->
                                         ->
                                         ->
                                         ->
                                         ->
                                         -> ('loki',2,4,4,4,4);
Query OK, 1 row affected (0.0091 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------+-------+----------+---------+-----+-----+
| id | name | genre | director | country | yor | yoe |
+----+------+-------+----------+---------+-----+-----+
|  1 | loki |     2 |        4 |       4 |   4 |   4 |
+----+------+-------+----------+---------+-----+-----+
1 row in set (0.0034 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------+-------+----------+---------+-----+-----+
| id | name | genre | director | country | yor | yoe |
+----+------+-------+----------+---------+-----+-----+
|  1 | loki |     2 |        4 |       4 |   4 |   4 |
+----+------+-------+----------+---------+-----+-----+
1 row in set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > drop id 1;
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'id 1' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > delete from series where id=1;
Query OK, 1 row affected (0.0082 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
Empty set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe director;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0131 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table genre(id int not null auto_increment,name varchar(256)not null,primary KEY(id));
Query OK, 0 rows affected (0.0384 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert insert into genre(name)values('Thriller');
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'insert into genre(name)values('Thriller')' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into genre(name)values('Thriller');
Query OK, 1 row affected (0.0104 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe genre;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0073 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from genre;
+----+----------+
| id | name     |
+----+----------+
|  1 | Thriller |
+----+----------+
1 row in set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into genre(name)values('comedy');
Query OK, 1 row affected (0.0063 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into genre(name)values('horror');
Query OK, 1 row affected (0.0063 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into genre(name)values('sci-fi');
Query OK, 1 row affected (0.0063 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into genre(name)values('adventure');
Query OK, 1 row affected (0.0070 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into genre(name)values('romance');
Query OK, 1 row affected (0.0083 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from genre;
+----+-----------+
| id | name      |
+----+-----------+
|  1 | Thriller  |
|  2 | comedy    |
|  3 | horror    |
|  4 | sci-fi    |
|  5 | adventure |
|  6 | romance   |
+----+-----------+
6 rows in set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from country;
Empty set (0.0045 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into country(name)values('INDIA');
Query OK, 1 row affected (0.0065 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into country(name)values('south_korea');
Query OK, 1 row affected (0.0055 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into country(name)values('german');
Query OK, 1 row affected (0.0066 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into country(name)values('usa');
Query OK, 1 row affected (0.0072 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into country(name)values('japanese');
Query OK, 1 row affected (0.0062 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from country;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | INDIA       |
|  2 | south_korea |
|  3 | german      |
|  4 | usa         |
|  5 | japanese    |
+----+-------------+
5 rows in set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table status(id int auto_increment not null,primary key(id));
Query OK, 0 rows affected (0.0624 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL >
 MySQL  localhost:3306 ssl  seriesdb  SQL >
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table status(id int auto_increment not null,name varchar(256)not null ,primary key(id));
ERROR: 1050 (42S01): Table 'status' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe status;
+-------+------+------+-----+---------+----------------+
| Field | Type | Null | Key | Default | Extra          |
+-------+------+------+-----+---------+----------------+
| id    | int  | NO   | PRI | NULL    | auto_increment |
+-------+------+------+-----+---------+----------------+
1 row in set (0.0062 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table status(name varchar(256)not null ,primary key(id));
ERROR: 1050 (42S01): Table 'status' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > delete table status;
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'table status' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > delete table status from series database;
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'table status from series database' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > drop table status;
Query OK, 0 rows affected (0.0309 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe status;
ERROR: 1146 (42S02): Table 'seriesdb.status' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table status(id int auto_increment not null,name varchar(256)not null ,primary key(id));
Query OK, 0 rows affected (0.0366 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe status;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0023 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into status (name)values('available');
Query OK, 1 row affected (0.0077 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into status (name)values('unavailable');
Query OK, 1 row affected (0.0069 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe status;
+-------+--------------+------+-----+---------+----------------+
| Field | Type         | Null | Key | Default | Extra          |
+-------+--------------+------+-----+---------+----------------+
| id    | int          | NO   | PRI | NULL    | auto_increment |
| name  | varchar(256) | NO   |     | NULL    |                |
+-------+--------------+------+-----+---------+----------------+
2 rows in set (0.0089 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from status;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | available   |
|  2 | unavailable |
+----+-------------+
2 rows in set (0.0034 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe series;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int          | NO   | PRI | NULL    | auto_increment |
| name     | varchar(256) | NO   |     | NULL    |                |
| genre    | int          | NO   |     | NULL    |                |
| director | int          | NO   |     | NULL    |                |
| country  | int          | NO   |     | NULL    |                |
| yor      | int          | NO   |     | NULL    |                |
| yoe      | int          | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
7 rows in set (0.0018 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series ;
Empty set (0.0035 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,gen)values('unavailable');                                           insert into series (name,genr)values('unavailable');                                          insert into series (name,genre)values('unavailable');                                         insert into series (name,genr)values('unavailable');                                          in
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Loki',1,'kate_herron',4,1,2021);
ERROR: 1054 (42S22): Unknown column 'status' in 'field list'
 MySQL  localhost:3306 ssl  seriesdb  SQL > ALTER TABLE table_name
                                         -> ADD column_name datatype;
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'datatype' at line 2
 MySQL  localhost:3306 ssl  seriesdb  SQL > ALTER TABLE series ADD status varchar(256);
Query OK, 0 rows affected (0.0269 sec)

Records: 0  Duplicates: 0  Warnings: 0
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series ;
Empty set (0.0030 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Loki',1,'kate_herron',4,1,2021);
ERROR: 1136 (21S01): Column count doesn't match value count at row 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,'kate_herron',4,1,2021);
ERROR: 1366 (HY000): Incorrect integer value: 'kate_herron' for column 'director' at row 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,kate_herron,4,1,2021);
ERROR: 1054 (42S22): Unknown column 'kate_herron' in 'field list'
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Loki',1,'kate_herron',4,1,2021);
ERROR: 1136 (21S01): Column count doesn't match value count at row 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,kate_herron,4,1,2021);
ERROR: 1054 (42S22): Unknown column 'kate_herron' in 'field list'
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,kateherron,4,1,2021);
ERROR: 1054 (42S22): Unknown column 'kateherron' in 'field list'
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,'kateherron',4,1,2021);
ERROR: 1366 (HY000): Incorrect integer value: 'kateherron' for column 'director' at row 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > drop table director;
Query OK, 0 rows affected (0.0297 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table director(id int  auto_increment not null,name varchar(256)not null,primary KEY(id));
Query OK, 0 rows affected (0.0368 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into director (name)values('kate_herron');
Query OK, 1 row affected (0.0103 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into director (name)values('otto_bathrust');
Query OK, 1 row affected (0.0058 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into director (name)values('dough_elin');
Query OK, 1 row affected (0.0073 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into director (name)values('frank_darabhart');
Query OK, 1 row affected (0.0070 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into director (name)values('alan_taylor');
Query OK, 1 row affected (0.0066 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into director (name)values('todd_A');
Query OK, 1 row affected (0.0077 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from director;
+----+-----------------+
| id | name            |
+----+-----------------+
|  1 | kate_herron     |
|  2 | otto_bathrust   |
|  3 | dough_elin      |
|  4 | frank_darabhart |
|  5 | alan_taylor     |
|  6 | todd_A          |
+----+-----------------+
6 rows in set (0.0033 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,'kateherron',4,1,2021);
ERROR: 1366 (HY000): Incorrect integer value: 'kateherron' for column 'director' at row 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,1,4,1,2021);
ERROR: 1364 (HY000): Field 'yoe' doesn't have a default value
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,1,4,1,2021,-);
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ')' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor)values('Loki',1,1,4,1,2021,2021);
ERROR: 1136 (21S01): Column count doesn't match value count at row 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Loki',1,1,4,1,2021,2021);
Query OK, 1 row affected (0.0052 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------+-------+----------+---------+------+------+--------+
| id | name | genre | director | country | yor  | yoe  | status |
+----+------+-------+----------+---------+------+------+--------+
|  2 | Loki |     1 |        1 |       4 | 2021 | 2021 | 1      |
+----+------+-------+----------+---------+------+------+--------+
1 row in set (0.0009 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Peaky_blinders',1,2,4,2,2021,2022);
Query OK, 1 row affected (0.0050 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+----------------+-------+----------+---------+------+------+--------+
| id | name           | genre | director | country | yor  | yoe  | status |
+----+----------------+-------+----------+---------+------+------+--------+
|  2 | Loki           |     1 |        1 |       4 | 2021 | 2021 | 1      |
|  3 | Peaky_blinders |     1 |        2 |       4 | 2021 | 2022 | 2      |
+----+----------------+-------+----------+---------+------+------+--------+
2 rows in set (0.0010 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('entourage',1,3,4,2,2004,2011);
Query OK, 1 row affected (0.0037 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('the_walking_dead',3,4,4,1,2010,2022);
Query OK, 1 row affected (0.0051 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('game_of_thrones',1,5,4,2,2011,2019);
Query OK, 1 row affected (0.0047 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('bloodline',3,6,4,1,2015,2019);
Query OK, 1 row affected (0.0056 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+------+------+--------+
| id | name             | genre | director | country | yor  | yoe  | status |
+----+------------------+-------+----------+---------+------+------+--------+
|  2 | Loki             |     1 |        1 |       4 | 2021 | 2021 | 1      |
|  3 | Peaky_blinders   |     1 |        2 |       4 | 2021 | 2022 | 2      |
|  4 | entourage        |     1 |        3 |       4 | 2004 | 2011 | 2      |
|  5 | the_walking_dead |     3 |        4 |       4 | 2010 | 2022 | 1      |
|  6 | game_of_thrones  |     1 |        5 |       4 | 2011 | 2019 | 2      |
|  7 | bloodline        |     3 |        6 |       4 | 2015 | 2019 | 1      |
+----+------------------+-------+----------+---------+------+------+--------+
6 rows in set (0.0010 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+------+------+--------+
| id | name             | genre | director | country | yor  | yoe  | status |
+----+------------------+-------+----------+---------+------+------+--------+
|  2 | Loki             |     1 |        1 |       4 | 2021 | 2021 | 1      |
|  3 | Peaky_blinders   |     1 |        2 |       4 | 2021 | 2022 | 2      |
|  4 | entourage        |     1 |        3 |       4 | 2004 | 2011 | 2      |
|  5 | the_walking_dead |     3 |        4 |       4 | 2010 | 2022 | 1      |
|  6 | game_of_thrones  |     1 |        5 |       4 | 2011 | 2019 | 2      |
|  7 | bloodline        |     3 |        6 |       4 | 2015 | 2019 | 1      |
+----+------------------+-------+----------+---------+------+------+--------+
6 rows in set (0.0014 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int auto_increment not null,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256) not null,yor int not null,yoe int not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > drop table series;
Query OK, 0 rows affected (0.0311 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
ERROR: 1146 (42S02): Table 'seriesdb.series' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int auto_increment not null,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256) not null,yor int not null,yoe int not null, primary KEY(id));
Query OK, 0 rows affected (0.0259 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
Empty set (0.0061 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(status varchar(256) not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(status varchar(256) not null, primary KEY(id));
ERROR: 1050 (42S01): Table 'series' already exists
 MySQL  localhost:3306 ssl  seriesdb  SQL > describe series;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int          | NO   | PRI | NULL    | auto_increment |
| name     | varchar(256) | NO   |     | NULL    |                |
| genre    | int          | NO   |     | NULL    |                |
| director | int          | NO   |     | NULL    |                |
| country  | int          | NO   |     | NULL    |                |
| status   | varchar(256) | NO   |     | NULL    |                |
| yor      | int          | NO   |     | NULL    |                |
| yoe      | int          | NO   |     | NULL    |                |
+----------+--------------+------+-----+---------+----------------+
8 rows in set (0.0073 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
Empty set (0.0010 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from status;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | available   |
|  2 | unavailable |
+----+-------------+
2 rows in set (0.0039 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('bloodline',3,6,4,1,2015,2019);
Query OK, 1 row affected (0.0086 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('bloodline',3,6,4,1,2015,2019);
Query OK, 1 row affected (0.0051 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from status;
+----+-------------+
| id | name        |
+----+-------------+
|  1 | available   |
|  2 | unavailable |
+----+-------------+
2 rows in set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('game_of_thrones',1,5,4,2,2011,2019);
Query OK, 1 row affected (0.0066 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('the_walking_dead',3,4,4,1,2010,2022);
Query OK, 1 row affected (0.0056 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('game_of_thrones',1,5,4,2,2011,2019);
Query OK, 1 row affected (0.0046 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('entourage',1,3,4,2,2004,2011);
Query OK, 1 row affected (0.0057 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Peaky_blinders',1,2,4,2,2021,2022);
Query OK, 1 row affected (0.0046 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Loki',1,1,4,1,2021,2021);
Query OK, 1 row affected (0.0060 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+------+------+
| id | name             | genre | director | country | status | yor  | yoe  |
+----+------------------+-------+----------+---------+--------+------+------+
|  1 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
|  2 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
|  3 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  4 | the_walking_dead |     3 |        4 |       4 | 1      | 2010 | 2022 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  6 | entourage        |     1 |        3 |       4 | 2      | 2004 | 2011 |
|  7 | Peaky_blinders   |     1 |        2 |       4 | 2      | 2021 | 2022 |
|  8 | Loki             |     1 |        1 |       4 | 1      | 2021 | 2021 |
+----+------------------+-------+----------+---------+--------+------+------+
8 rows in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > delete from series where id=1;
Query OK, 1 row affected (0.0059 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+------+------+
| id | name             | genre | director | country | status | yor  | yoe  |
+----+------------------+-------+----------+---------+--------+------+------+
|  2 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
|  3 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  4 | the_walking_dead |     3 |        4 |       4 | 1      | 2010 | 2022 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  6 | entourage        |     1 |        3 |       4 | 2      | 2004 | 2011 |
|  7 | Peaky_blinders   |     1 |        2 |       4 | 2      | 2021 | 2022 |
|  8 | Loki             |     1 |        1 |       4 | 1      | 2021 | 2021 |
+----+------------------+-------+----------+---------+--------+------+------+
7 rows in set (0.0019 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  2 | bloodline        | horror   | todd_A          | usa     | available   |
|  3 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  4 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  7 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  8 | Loki             | Thriller | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0049 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor;
ERROR: 1146 (42S02): Table 'seriesdb.yor' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor;
ERROR: 1146 (42S02): Table 'seriesdb.yor' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id;
ERROR: 1146 (42S02): Table 'seriesdb.yor' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+------+------+
| id | name             | genre | director | country | status | yor  | yoe  |
+----+------------------+-------+----------+---------+--------+------+------+
|  2 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
|  3 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  4 | the_walking_dead |     3 |        4 |       4 | 1      | 2010 | 2022 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  6 | entourage        |     1 |        3 |       4 | 2      | 2004 | 2011 |
|  7 | Peaky_blinders   |     1 |        2 |       4 | 2      | 2021 | 2022 |
|  8 | Loki             |     1 |        1 |       4 | 1      | 2021 | 2021 |
+----+------------------+-------+----------+---------+--------+------+------+
7 rows in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor;
ERROR: 1146 (42S02): Table 'seriesdb.yor' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  2 | bloodline        | horror   | todd_A          | usa     | available   |
|  3 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  4 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  7 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  8 | Loki             | Thriller | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table yor(id int  auto_increment not null,int not null,primary KEY(id));
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'int not null,primary KEY(id))' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table yor(id int  auto_increment not null,name int not null,primary KEY(id));
Query OK, 0 rows affected (0.0439 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table yoe(id int  auto_increment not null,name int not null,primary KEY(id));
Query OK, 0 rows affected (0.0389 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name)values(2000);
ERROR: 1364 (HY000): Field 'genre' doesn't have a default value
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2000);
Query OK, 1 row affected (0.0106 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2008);
Query OK, 1 row affected (0.0062 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2009);
Query OK, 1 row affected (0.0080 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2015);
Query OK, 1 row affected (0.0063 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2013);
Query OK, 1 row affected (0.0054 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2006);
Query OK, 1 row affected (0.0078 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yor (name)values(2007);
Query OK, 1 row affected (0.0069 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2008);
Query OK, 1 row affected (0.0178 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2016);
Query OK, 1 row affected (0.0062 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2012);
Query OK, 1 row affected (0.0058 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2018);
Query OK, 1 row affected (0.0068 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2016);
Query OK, 1 row affected (0.0078 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2009);
Query OK, 1 row affected (0.0063 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into yoe (name)values(2009);
Query OK, 1 row affected (0.0064 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from yoe;
+----+------+
| id | name |
+----+------+
|  1 | 2008 |
|  2 | 2016 |
|  3 | 2012 |
|  4 | 2018 |
|  5 | 2016 |
|  6 | 2009 |
|  7 | 2009 |
+----+------+
7 rows in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from yor;
+----+------+
| id | name |
+----+------+
|  1 | 2000 |
|  2 | 2008 |
|  3 | 2009 |
|  4 | 2015 |
|  5 | 2013 |
|  6 | 2006 |
|  7 | 2007 |
+----+------+
7 rows in set (0.0034 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+------+------+
| id | name             | genre | director | country | status | yor  | yoe  |
+----+------------------+-------+----------+---------+--------+------+------+
|  2 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
|  3 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  4 | the_walking_dead |     3 |        4 |       4 | 1      | 2010 | 2022 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  6 | entourage        |     1 |        3 |       4 | 2      | 2004 | 2011 |
|  7 | Peaky_blinders   |     1 |        2 |       4 | 2      | 2021 | 2022 |
|  8 | Loki             |     1 |        1 |       4 | 1      | 2021 | 2021 |
+----+------------------+-------+----------+---------+--------+------+------+
7 rows in set (0.0036 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('bloodline',3,6,4,1,2015,2019);
Query OK, 1 row affected (0.0049 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+------+------+
| id | name             | genre | director | country | status | yor  | yoe  |
+----+------------------+-------+----------+---------+--------+------+------+
|  2 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
|  3 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  4 | the_walking_dead |     3 |        4 |       4 | 1      | 2010 | 2022 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      | 2011 | 2019 |
|  6 | entourage        |     1 |        3 |       4 | 2      | 2004 | 2011 |
|  7 | Peaky_blinders   |     1 |        2 |       4 | 2      | 2021 | 2022 |
|  8 | Loki             |     1 |        1 |       4 | 1      | 2021 | 2021 |
|  9 | bloodline        |     3 |        6 |       4 | 1      | 2015 | 2019 |
+----+------------------+-------+----------+---------+--------+------+------+
8 rows in set (0.0036 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > drop table series;
Query OK, 0 rows affected (0.0524 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
ERROR: 1146 (42S02): Table 'seriesdb.series' doesn't exist
 MySQL  localhost:3306 ssl  seriesdb  SQL > create table series(id int auto_increment not null,name varchar(256)not null,genre int not null ,director int not null,country int not null,status varchar(256) not null,yor int not null,yoe int not null, primary KEY(id));
Query OK, 0 rows affected (0.0265 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
Empty set (0.0117 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('bloodline',3,6,4,1,1,1);
Query OK, 1 row affected (0.0046 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Loki',1,1,4,1,2,2);
Query OK, 1 row affected (0.0059 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('Peaky_blinders',1,2,4,2,3,3);
Query OK, 1 row affected (0.0063 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('entourage',1,3,4,2,4,4);
Query OK, 1 row affected (0.0049 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('game_of_thrones',1,5,4,2,5,5);
Query OK, 1 row affected (0.0034 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('the_walking_dead',3,4,4,1,6,6);
Query OK, 1 row affected (0.0046 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > insert into series (name,genre,director,country,status,yor,yoe)values('stranger_things',3,1,4,1,7,7);
Query OK, 1 row affected (0.0050 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+-----+-----+
| id | name             | genre | director | country | status | yor | yoe |
+----+------------------+-------+----------+---------+--------+-----+-----+
|  1 | bloodline        |     3 |        6 |       4 | 1      |   1 |   1 |
|  2 | Loki             |     1 |        1 |       4 | 1      |   2 |   2 |
|  3 | Peaky_blinders   |     1 |        2 |       4 | 2      |   3 |   3 |
|  4 | entourage        |     1 |        3 |       4 | 2      |   4 |   4 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      |   5 |   5 |
|  6 | the_walking_dead |     3 |        4 |       4 | 1      |   6 |   6 |
|  7 | stranger_things  |     3 |        1 |       4 | 1      |   7 |   7 |
+----+------------------+-------+----------+---------+--------+-----+-----+
7 rows in set (0.0033 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  1 | bloodline        | horror   | todd_A          | usa     | available   |
|  2 | Loki             | Thriller | kate_herron     | usa     | available   |
|  3 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  4 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  7 | stranger_things  | horror   | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0043 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  1 | bloodline        | horror   | todd_A          | usa     | available   |
|  2 | Loki             | Thriller | kate_herron     | usa     | available   |
|  3 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  4 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  7 | stranger_things  | horror   | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  1 | bloodline        | horror   | todd_A          | usa     | available   |
|  2 | Loki             | Thriller | kate_herron     | usa     | available   |
|  3 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  4 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  7 | stranger_things  | horror   | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0027 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series;
+----+------------------+-------+----------+---------+--------+-----+-----+
| id | name             | genre | director | country | status | yor | yoe |
+----+------------------+-------+----------+---------+--------+-----+-----+
|  1 | bloodline        |     3 |        6 |       4 | 1      |   1 |   1 |
|  2 | Loki             |     1 |        1 |       4 | 1      |   2 |   2 |
|  3 | Peaky_blinders   |     1 |        2 |       4 | 2      |   3 |   3 |
|  4 | entourage        |     1 |        3 |       4 | 2      |   4 |   4 |
|  5 | game_of_thrones  |     1 |        5 |       4 | 2      |   5 |   5 |
|  6 | the_walking_dead |     3 |        4 |       4 | 1      |   6 |   6 |
|  7 | stranger_things  |     3 |        1 |       4 | 1      |   7 |   7 |
+----+------------------+-------+----------+---------+--------+-----+-----+
7 rows in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  1 | bloodline        | horror   | todd_A          | usa     | available   |
|  2 | Loki             | Thriller | kate_herron     | usa     | available   |
|  3 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  4 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  7 | stranger_things  | horror   | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0009 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select*from series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where country.id=4;
ERROR: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'from series inner join genre on series.genre=genre.id join director on series.di' at line 1
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where country.id=4;
+----+------------------+----------+-----------------+---------+-------------+
| id | name             | genre    | director        | country | status      |
+----+------------------+----------+-----------------+---------+-------------+
|  1 | bloodline        | horror   | todd_A          | usa     | available   |
|  2 | Loki             | Thriller | kate_herron     | usa     | available   |
|  3 | Peaky_blinders   | Thriller | otto_bathrust   | usa     | unavailable |
|  4 | entourage        | Thriller | dough_elin      | usa     | unavailable |
|  5 | game_of_thrones  | Thriller | alan_taylor     | usa     | unavailable |
|  6 | the_walking_dead | horror   | frank_darabhart | usa     | available   |
|  7 | stranger_things  | horror   | kate_herron     | usa     | available   |
+----+------------------+----------+-----------------+---------+-------------+
7 rows in set (0.0009 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where genre.id=4;
Empty set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where genre.id=3;
+----+------------------+--------+-----------------+---------+-----------+
| id | name             | genre  | director        | country | status    |
+----+------------------+--------+-----------------+---------+-----------+
|  1 | bloodline        | horror | todd_A          | usa     | available |
|  6 | the_walking_dead | horror | frank_darabhart | usa     | available |
|  7 | stranger_things  | horror | kate_herron     | usa     | available |
+----+------------------+--------+-----------------+---------+-----------+
3 rows in set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where yoe.id=3;
+----+----------------+----------+---------------+---------+-------------+
| id | name           | genre    | director      | country | status      |
+----+----------------+----------+---------------+---------+-------------+
|  3 | Peaky_blinders | Thriller | otto_bathrust | usa     | unavailable |
+----+----------------+----------+---------------+---------+-------------+
1 row in set (0.0010 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where yoe.id=2;
+----+------+----------+-------------+---------+-----------+
| id | name | genre    | director    | country | status    |
+----+------+----------+-------------+---------+-----------+
|  2 | Loki | Thriller | kate_herron | usa     | available |
+----+------+----------+-------------+---------+-----------+
1 row in set (0.0008 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where yoe=2010 ;
Empty set (0.0012 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where yoe=2009 ;
Empty set (0.0006 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL > select series.id as id,series.name as name,genre.name as genre,director.name as director , country.name as country,status.name as status from series inner join genre on series.genre=genre.id join director on series.director=director.id join country on series.country=country.id join status on series.status=status.id join yor on series.yor=yor.id join yoe on series.yoe=yoe.id where yor=2009 and yoe=2007 ;
Empty set (0.0007 sec)
 MySQL  localhost:3306 ssl  seriesdb  SQL >

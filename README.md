# MySQL Project

## Resources
Read or watch:

- [MySQL Cheatsheet](https://intranet.alxswe.com/rltoken/8w9di_hk19DIMSBEV3EayQ)
- [MySQL Performance: How To Leverage MySQL Database Indexing](https://intranet.alxswe.com/rltoken/2GJbZ48zRPA70o2YhTdH7g)
- [Stored Procedure](https://intranet.alxswe.com/rltoken/K180X2OCzb6gzPngjn-EIg)
- [Triggers](https://intranet.alxswe.com/rltoken/cJ1qA4o-rRm4rWIsqYKSZg)
- [Views](https://intranet.alxswe.com/rltoken/vHg1z3UAOcWMvOt8xZHeiA)
- [Functions and Operators](https://intranet.alxswe.com/rltoken/g-c1m6iljScpi4LeqxBRqQ)
- [Trigger Syntax and Examples](https://intranet.alxswe.com/rltoken/gLVwKjQfRL0Jr_nWqAS7VQ)
- [CREATE TABLE Statement](https://intranet.alxswe.com/rltoken/X789nJ22H6HVh1uCQPl0lg)
- [CREATE PROCEDURE and CREATE FUNCTION Statements](https://intranet.alxswe.com/rltoken/mfrWMt1KL3NHXblJykMgZg)
- [CREATE INDEX Statement](https://intranet.alxswe.com/rltoken/oCu8Rg9WfKyF4BhTt8dZGQ)
- [CREATE VIEW Statement](https://intranet.alxswe.com/rltoken/FEZNlZFKZmD1ISnLINkCwQ)

## Learning Objectives
By the end of this project, you should be able to explain the following concepts to anyone, without the help of Google:

### General
- How to create tables with constraints
- How to optimize queries by adding indexes
- What stored procedures and functions are, and how to implement them in MySQL
- What views are, and how to implement them in MySQL
- What triggers are, and how to implement them in MySQL

## Requirements
### General
- All your files will be executed on Ubuntu 18.04 LTS using MySQL 5.7 (version 5.7.30)
- All your files should end with a new line
- All your SQL queries should have a comment just before them (i.e. syntax above)
- All your files should start with a comment describing the task
- All SQL keywords should be in uppercase (SELECT, WHERE, etc.)
- A `README.md` file, at the root of the project folder, is mandatory
- The length of your files will be tested using `wc`

## More Info

### Comments for your SQL file:
```sql
-- 3 first students in the Batch ID=3
-- because Batch 3 is the best!
SELECT id, name FROM students WHERE batch_id = 3 ORDER BY created_at DESC LIMIT 3;
```

### Use “container-on-demand” to run MySQL
1. Request a container with Ubuntu 18.04 - Python 3.7
2. Connect via SSH or via the WebTerminal
3. In the container, start MySQL before using it:
    ```sh
    $ service mysql start
    * MySQL Community Server 5.7.30 is started
    ```

4. Run SQL scripts:
    ```sh
    $ cat 0-list_databases.sql | mysql -uroot -p my_database
    Enter password:
    Database
    information_schema
    mysql
    performance_schema
    sys
    ```

### In the container, credentials are root/root

### How to import a SQL dump
```sh
$ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
Enter password:
$ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
Enter password:
$ echo "SELECT * FROM tv_genres" | mysql -uroot -p hbtn_0d_tvshows
Enter password:
id  name
1   Drama
2   Mystery
3   Adventure
4   Fantasy
5   Comedy
6   Crime
7   Suspense
8   Thriller
```

Feel free to explore and learn more about MySQL using the provided resources and by following the instructions in this README.
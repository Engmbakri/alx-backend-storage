Concepts
For this project, look at these concepts:

Advanced SQL
Resources
Read or watch:

MySQL cheatsheet
MySQL Performance: How To Leverage MySQL Database Indexing
Stored Procedure
Triggers
Views
Functions and Operators
Trigger Syntax and Examples
CREATE TABLE Statement
CREATE PROCEDURE and CREATE FUNCTION Statements
CREATE INDEX Statement
CREATE VIEW Statement
Requirement
General
Files executed on Ubuntu 18.04 LTS using MySQL 5.7 (version 5.7.30)
Files must end with a new line
All SQL queries should have a comment just before (i.e. syntax above)
Files should start with comment describing tasks
All SQL keywords should be in uppercase (SELECT, WHERE...)
Mandatory README.md file
Length of files tested using wc
More Info
Comments for your SQL file:
$ cat my_script.sql
-- 3 first students in the Batch ID=3
-- because Batch 3 is the best
SELECT id, name FROM students WHERE batch_id = 3 ORDER BY created_at DESC LIMIT 3;
$
Use "container-on-demand" to run MySQL
Ask for container Ubuntu 18.04 - Python 3.7
Connect via SSH
Or via the Web Terminal
In the container, start MySQL before playing with it
$ service mysql start
* MySQL Community Server 5.7.30 is started
$
$ cat 0-list_databases.sql | mysql -uroot -p my_database
Enter password:
Database
information_schema
mysql
performance_schema
sys
$
In the container, credentials are root/root

How to import a SQL dump
$ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
Enter password:
$ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
Enter password:
$ echo "SELECT * FROM tv_genres" | mysql -uroot -p hbtn_0d_tvshows
Enter password:
id name
1 Drama
2 Mystery
3 Adventure
4 Fantasy
5 Comedy
6 Crime
7 Suspense
8 Thriller
$

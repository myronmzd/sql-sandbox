To see all the tables that have been created in a database, the exact command depends on which database system (DBMS) you are using. Here are the most common ways for popular databases:

MySQL / MariaDB:
```bash
SHOW TABLES;
```
PostgreSQL:

```bash
\dt
```

Or, as a SQL query:
```bash
SELECT table_name FROM information_schema.tables WHERE table_schema = 'public';
```
SQLite:
```bash
.tables
```
Or, as a SQL query:
```bash
SELECT name FROM sqlite_master WHERE type='table';
```
SQL Server (MSSQL):
```bash
SELECT name FROM sqlite_master WHERE type='table';
```
Or:

Oracle:
```bash
SELECT * FROM information_schema.tables WHERE table_type = 'BASE TABLE';
```



Wrap the script in a single transaction if possible:
```sql
BEGIN;
-- Chinook_PostgreSql.sql contents here
COMMIT;
```
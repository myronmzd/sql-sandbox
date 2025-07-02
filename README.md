# sql-sandbox
Keep everything SQL‑lab–related inside C:\sql-sandbox and you can nuke or back‑up your entire playground with one folder.


# Launch both servers:

```powershell

cd C:\sql-sandbox
docker compose up -d          # starts pg on 5432, MySQL on 3306
```

# Shut them down any time:

```powershell
docker compose down
```

#  Check Container Logs

```bash
docker logs pg_lab
docker logs mysql_lab
```

# to connect to them as extentions for vs code 


# PostgreSQL

Install the PostgreSQL extension for VS Code.
Add a new connection with:
Host: localhost
Port: 5432
User: bob
Password: bob12
Database: sandbox

# MySQL

Install the MySQL extension for VS Code or SQLTools.
Add a new connection with:
Host: localhost
Port: 3306
User: bob (or root)
Password: bob12
Database: sandbox


2. Use the Terminal
PostgreSQL
You’ll get a psql prompt where you can type SQL queries.

```bash 
docker exec -it pg_lab psql -U bob -d sandbox
```

MySQL
You’ll get a MySQL prompt for queries.

```bash
docker exec -it mysql_lab mysql -u bob -p
# Enter password: bob12
use sandbox;
```
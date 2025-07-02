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

#  Seed with sample data

```bash
# PostgreSQL – dvdrental example
docker exec -i pg_lab psql -U bob -d sandbox < dvdrental-schema.sql

# MySQL – Sakila example
docker exec -i mysql_lab mysql -u root -psecret sandbox < sakila-schema.sql

```
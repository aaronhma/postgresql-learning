# psql shell

## Utility

```bash
# Exit the postgres prompt
\q

# help menu
\?

# List all of your actual databases.
\list

# Connect to another database.
\c database_name

# List the relations of your currently connected database.
\d

# Shows information for a specific table.
\d table_name
```

## System

```bash
# create the superuser with its credentials
CREATE USER postgres WITH SUPERUSER PASSWORD 'postgres';

# create a new role
CREATE ROLE postgres;
```

## Connected to Database

```bash
# connect to database name postgres
psql postgres

# select data from database table
SELECT * FROM table_name;
```

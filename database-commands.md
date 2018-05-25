# Database Commands

```bash
# initialize the physical space on your hard-disk to allocate
# databases Therefore, create the default postgres database
initdb /usr/local/var/postgres

# pg server start
pg_ctl -D /usr/local/var/postgres start

# pg server stop
pg_ctl -D /usr/local/var/postgres stop

# connect to database name postgres
psql postgres
```

## Restoration Of A Database

```bash
# full data restoration
pg_rstore -U username -d database_name /PATH/TO/UNZIPPED/FOLDER

# only schema restoration
pg_rstore -U username -d database_name -s /PATH/TO/UNZIPPED/FOLDER

# full data restoration with database dump
pg_rstore -U username -d database_name -C /TO/DUMP_FILE
```

## How to Copy & Import Data Between Database

```bash
# Copy table data to local csv file without header with all column data
COPY table_name TO '/Users/your_root_name/Downloads/sql/table_name.csv' DELIMITERS ',' CSV;

# Copy table to local csv file with header with specific column data
COPY table_name(column_name, column_name, ...) TO '/Users/your_root_name/Downloads/sql/table_name.csv' DELIMITERS ',' CSV HEADER;
```

```bash
# Copy table data to local csv file without header with all column data
COPY table_name FROM '/Users/your_root_name/Downloads/sql/table_name.csv' DELIMITERS ',' CSV;

# Copy table to local csv file with header with specific column data
COPY table_name(column_name, column_name, ...) FROM '/Users/your_root_name/Downloads/sql/table_name.csv' DELIMITERS ',' CSV HEADER;
```

## VACUUM table or database

```bash
# vacuum a specific table, instead of the entire database
VACUUM table_name;

# free up the space within the table,  allocate the unused space back to the operating system
VACUUM FULL table_name;
```

## Delete table data from database

```bash
DELETE FROM table_name;
```

## Select Statement

``` bash
SELECT * FROM table_name WHERE column_name > 11 AND condition;
```
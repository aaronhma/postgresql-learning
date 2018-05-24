# Database Commands

```bash
# initialize postgresdb
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

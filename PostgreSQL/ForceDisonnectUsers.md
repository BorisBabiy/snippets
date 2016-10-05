## Force disconnect users

### PostgreSQL 9.1 and below:

```sql
SELECT pg_terminate_backend(pg_stat_activity.procpid)
FROM pg_stat_activity
WHERE pg_stat_activity.datname = 'TARGET_DB'
  AND procpid <> pg_backend_pid();
```

### PostgreSQL 9.2 and above:

```sql
SELECT pg_terminate_backend(pg_stat_activity.pid)
FROM pg_stat_activity
WHERE pg_stat_activity.datname = 'TARGET_DB'
  AND pid <> pg_backend_pid();
```

original post on [http://stackoverflow.com/](http://stackoverflow.com/a/5408501)

## Might be helpful 

Also you can find IP address of the users connected to the database

```sql
select client_addr from pg_stat_activity where datname = 'TARGET_DB';
```

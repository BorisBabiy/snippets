## Backup

```shell
export PGPASSWORD=password
pg_dump -Fc --no-acl --no-owner -h host -U user database > database.dump
```

on localhost as postgres user:

```shell
sudo su - postgres 
pg_dump -Fc --no-acl --no-owner database > database.dump
```

with timestamp in the file name

```shell
sudo su - postgres
pg_dump -Fc --no-acl --no-owner database > database-$(date +"%Y%m%d").dump

```

## Restore

```shell
pg_restore --verbose --clean --no-acl --no-owner -h localhost -U myuser -d database database.dump
```

on localhost as postgres user

```shell
pg_restore --verbose --clean --no-acl --no-owner -d database database.dump
```

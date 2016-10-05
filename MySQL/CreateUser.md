## Create user


```sql
GRANT ALL PRIVILEGES ON database_name.* TO 'user'@'localhost' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
```

```sql
GRANT ALL PRIVILEGES ON database_name.* TO 'user'@'%' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
```

In the second example `'%'` mean any host.  

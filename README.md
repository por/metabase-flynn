# Running metabase on Flynn

Create Flynn app:

```$ flynn create metabase```

Add Postgres database:

```$ flynn -a metabase resource add postgres```

Set required environment variables:

```
flynn -a metabase env set \
  MB_JETTY_PORT=8080 \
  MB_DB_TYPE=postgres \
  MB_DB_DBNAME={PGDATABASE} \
  MB_DB_PORT=5432 \
  MB_DB_PASS={PGPASSWORD} \
  MB_DB_USER={PGUSER} \
  MB_DB_HOST=leader.postgres.discoverd
```

# PostgreSQL Export

LIST ALL TABLES TO EXPORT - WINDOWS

```
SELECT 'COPY public.'||table_name||' TO E''C:\\Dados\\'||table_name||'.csv'' WITH DELIMITER AS '';'' CSV HEADER;'
  FROM information_schema.tables
  WHERE table_schema='public'
  AND table_type='BASE TABLE';
```

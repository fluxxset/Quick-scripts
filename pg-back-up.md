# backup 

```pg_dump -U dbuser -d dbname -f backup_file.sql```

# restore 

`psql -U dbuser -p 5432 -h 192.168.0.107  -d dbname < backup_file.sql`

## in case error occures 


-- Switch to the database
`\c dbname`

-- Grant privileges on the schema
`GRANT USAGE, CREATE ON SCHEMA public TO dbuser;`

-- Ensure the user owns the schema
`ALTER SCHEMA public OWNER TO dbuser;`

# PostgreSQL

* Insert record if not exists

```sql
INSERT INTO brand(name)
SELECT 'COSMIC MANSION'
WHERE NOT EXISTS(
        SELECT 1 FROM brand WHERE name = 'COSMIC MANSION'
    );
```

* Inser records with fixed value
   ```sql 
   insert into user_brand (username, brand)  select 'shivadbuser@sephora.com', id from brand;```
   
* Export table schema
```sql
pg_dump --schema-only --no-owner newness_nif_management > create_the_tables.sql
```

* Create database and user
```sql
CREATE DATABASE yourdbname;
CREATE USER youruser WITH ENCRYPTED PASSWORD 'yourpass';
GRANT ALL PRIVILEGES ON DATABASE yourdbname TO youruser;
```


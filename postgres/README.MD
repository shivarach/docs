# PostgreSQL

* Insert record if not exists

  `INSERT INTO brand(name)
SELECT 'COSMIC MANSION'
WHERE NOT EXISTS(
        SELECT 1 FROM brand WHERE name = 'COSMIC MANSION'
    );`

* Inser records with fixed value
   ```insert into user_brand (username, brand)  select 'shivadbuser@sephora.com', id from brand;```


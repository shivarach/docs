# PostgreSQL

* Insert record if not exists

  `INSERT INTO brand(name)
SELECT 'COSMIC MANSION'
WHERE NOT EXISTS(
        SELECT 1 FROM brand WHERE name = 'COSMIC MANSION'
    );`

# Docker MySQL Sample

## Usage

```bash
docker-compose up -d
docker-compose exec db mysql -u docker -p
```

## Sample Table

```bash
mysql> USE test_database
mysql> CREATE TABLE users (id INTEGER NOT NULL PRIMARY KEY, name CHAR(16));
mysql> CREATE TABLE orders (id INTEGER NOT NULL PRIMARY KEY, user_id INTEGER UNIQUE, product_id INTEGER, CONSTRAINT fk_user_id FOREIGN KEY (user_id) REFERENCES users (id));
mysql> SHOW CREATE TABLE orders;
```

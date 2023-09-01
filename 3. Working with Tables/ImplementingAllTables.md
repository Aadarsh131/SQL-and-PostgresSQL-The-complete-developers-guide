# Implementing the whole idea

### 1. Creating and inserting the values into `users` table
```sql
CREATE TABLE users (id SERIAL PRIMARY KEY, username VARCHAR(50));
```
> `SERIAL` is an identifier which will help to auto increment/decrement the id no. value with each new row update/delete resp, and also makes sure if the row with any id is deleted, another row with that same deleted id will never be created ever again

```sql
INSERT INTO
  users (username)
VALUES
  ('Aadarsh'),
  ('Priya'),
  ('Atul');
```

### 2. Creating and inserting the values into `photos` table
```sql
CREATE TABLE photos (
  id SERIAL PRIMARY KEY,
  url VARCHAR(200),
  user_id INTEGER REFERENCES users(id)
);
```
> user_id column will be storing the foreign key

> `REFERENCES <tablename>(<columnname>)` makes a connection/relation between the defined table with its defined column

```sql
INSERT INTO
  photos (url, user_id)
VALUES
  ('https://rewq34.jpg', 3),
  ('https://one.jpg', 1),
  ('https://two.jpg', 2),
  ('https://three.jpg', 1),
  ('https://four.jpg', 2),
  ('https://five.jpg', 3);
```

### To maintain data consistency
```sql
INSERT INTO
  photos (url, user_id)
VALUES
  ('https://lol.jpg', 999), /* error, as there is no user with id 999 */
  ('https://null.jpg', NULL),/*represents a photo associated to NO user */
```
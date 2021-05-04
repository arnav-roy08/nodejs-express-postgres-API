# nodejs-express-postgres-API

Setting up database: 
brew install postgresql
brew services start postgresql
psql postgres
postgres=# CREATE ROLE arnav WITH LOGIN PASSWORD 'password';
postgres=# \q
psql -d postgres -U arnav

CREATE DATABASE api;
\c api

api=>
CREATE TABLE userss (
  ID SERIAL PRIMARY KEY,
  name VARCHAR(30),
  email VARCHAR(30)
);





POST
curl --data "name=arnav&email=arnav@gmail.com" http://localhost:3000/users

PUT
curl -X PUT -d "name=arnav" -d "email=arnav@gmail.com" http://localhost:3000/users/1

DELETE
curl -X "DELETE" http://localhost:3000/users/1


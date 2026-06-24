psql Shell Commands:
sudo -u postgres psql
  \l -> List all available databases on the server
  \c dbname -> Connect / switch to a different database
  \dt -> List all tables in the currently connected database
  \d tablename -> Describe a specific table's schema, columns, and data types
  \du -> List all database users (roles) and their assign privileges
  \x -> Toggle expanded display mode.
  \? -> Show help documentation for all available commands
  \q -> Quit the psql terminal and return to the normal Linux prompt
Managing Users (ROLES):
  --Creating a new user in postgreSQL
  CREATE USER newTestUser WITH PASSWORD 'anyPass';
  --Updating the password of a user in postgreSQL
  ALTER USER newTestUser WITH PASSWORD 'newPass';
  --Make the user a SuperUser
  ALTER USER newTestUser WITH SUPERUSER;
  --Giving Permission to Create a DB
  ALTER USER newTestUser WITH CREATEDB;
  --Deleting a User
  DROP USER newTestUser;
  --Granting Permissions to work on a DB
  GRANT ALL PRIVILEGES ON DATABASE testDB TO newTestUser;

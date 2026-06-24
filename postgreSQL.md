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

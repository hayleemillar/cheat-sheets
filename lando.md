
# Lando Cheat Sheet

### Starting LEMP Stack
```bash
# Initialize a LEMP recipe using the latest CakePHP 2.0 version
lando init \
  --source remote \
  --remote-url git://github.com/cakephp/cakephp.git \
  --remote-options="--branch 2.x --depth 1" \
  --recipe lemp \
  --webroot . \
  --name my-first-lemp-app

# Start it up
lando start

# List information about this app.
lando info
```

### Accessing server-hosted app
```bash
lando ssh
```
Now you are within the working directory of your app.

### Accessing app's database
```bash
lando ssh -s database
mysql -u root
```

### Importing a Database
Move the database dump to the base directory of Lando project.
  
```bash
lando db-import sql-file-name.sql
```

### Clearing Cache
When altering CSS, some lando projects need to have their cache cleared manually.
```bash
lando drush cc all
```

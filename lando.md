
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
If the database you received has the extension tar.gz, unzip first. Then, import the unzipped .sql file using the command above.

### Clearing Cache
When altering CSS, some lando projects need to have their cache cleared manually.
```bash
lando drush cc all
```

### My local site is not working.
Check site/sites/default/settings.php.  
Check for differences between settings.php and settings.local.php.  
Check lando.yml, specificall drush and events configurations if present.


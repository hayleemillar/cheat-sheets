
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

### Starting an application
```bash
lando rebuild
```

### Importing a Database
Move the database dump to the base directory of Lando project.
  
```bash
lando db-import sql-file-name.sql
```
